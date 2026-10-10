---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through recommendation, implementation, verification, and handoff.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, automation, integration, or operational problem where the solution is not already clear. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the problem

Start with the underlying problem, not the proposed solution. When asked to “build X,” work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the situation meaningfully better?
- What constraints, dependencies, or affected systems matter?

Write a concise problem statement and descriptive requirements. Describe the desired outcome and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so directly.

Research available documentation, code, and authorized records before asking questions. If reviewing communications, tickets, or records about people, have a legitimate purpose and clear authorization; use only the minimum relevant sources and omit unrelated or sensitive personal details.

## 2. Assess priority and decision type

Decide whether the work is worth doing now. Consider severity, frequency, affected users, opportunity cost, existing alternatives, and the cost of delay. Treat “do nothing,” “deprioritize,” or “improve the workaround” as valid options.

Distinguish between:

- **Reversible decisions:** Small choices that are easy to change. Use reasonable judgment and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, migrations, public interfaces, long-lived settings, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation and document the rationale when appropriate.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operating procedures, and prior attempts. Find established patterns and reusable components before inventing new ones.

Identify compatibility requirements, deployment practices, privacy and security expectations, supported environments, ownership boundaries, monitoring, and rollback constraints. Respect access boundaries: do not expose source material or information beyond the audience authorized to receive it.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve current authentication, privacy, and data behavior.
- Must be feasible within the available delivery and maintenance capacity.
- Should avoid unnecessary dependencies and permanent configuration.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variants of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer instructions, a process change, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Building, buying, or integrating an existing service.

For ambiguous or high-impact problems, generate a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, major costs, dependencies, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that vary by runtime conditions.
- Validate inputs and fail clearly for invalid states. Do not hide programming errors by returning plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Place changes at the correct design boundary; avoid temporary fixes that create lasting complexity.

## 6. Evaluate and recommend

Compare viable options against the evaluation criteria. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep proposals direct and brief. Store durable proposals in the user’s chosen shared documentation system when review or collaboration is needed; otherwise provide them in the current workspace. Use a clear date-prefixed title, such as `10 Oct 2026: Solve — topic`.

**Readiness gate:** Do not implement until the recommendation is accepted, or the user has explicitly authorized implementation under an agreed decision rule. For analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, dependencies, migration and rollback strategy, test strategy, deployment steps, and ownership of follow-up actions.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, security, and failure behavior.

Do not claim success based only on code being written. State what was tested, the result, and what remains unverified. Commit, publish, or deploy only according to the user’s repository and release practices.

## 8. Audit and hand off

Before handoff, check that:

- The implemented scope matches the approved recommendation.
- Hard-to-reverse commitments received explicit approval.
- Tests cover the important success and failure paths.
- Sensitive information is not included in outputs or logs beyond the authorized boundary.
- Rollback, monitoring, and ownership are clear where relevant.

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail rather than temporary implementation notes.

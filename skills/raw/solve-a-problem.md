---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, recommendation, implementation, verification, and handoff, with an analysis-only stopping point when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user explicitly requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's proposed solution. If they ask to build something, work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would materially improve the situation?
- What constraints, dependencies, and success measures apply?

Write a concise problem statement and descriptive requirements. Describe the desired outcome and constraints, not an assumed implementation. If the proposed solution does not appear to address the real problem, say so clearly.

Ask only for information that cannot be found in authorized, relevant context such as project documentation, code, tests, or operating procedures. When reviewing communications or records about people, confirm a legitimate purpose and clear authorization; use only the minimum relevant sources, exclude unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Decide whether to solve it now

Assess severity, frequency, affected users, opportunity cost, current alternatives, and maintenance cost. Treat “do nothing,” “deprioritize,” or “improve the workaround” as valid options when the problem is low-impact or adequately handled.

Distinguish between decisions:

- **Reversible decisions:** Small choices that are easy to change. Use reasonable judgment and move forward.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, migrations, long-lived settings, security boundaries, external commitments, or vendor contracts. Pause for an explicit decision before implementation and record the rationale when appropriate.

If priority or direction is unclear, present the tradeoff to the responsible decision-maker before investing in substantial design or implementation.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, code, tests, deployment procedures, and previous attempts. Identify existing patterns, reusable components, compatibility expectations, ownership boundaries, security requirements, and monitoring practices.

Use the system’s established conventions unless there is a clear, documented reason to change them. Do not assume a new tool, dependency, or service is necessary before checking what existing capabilities can solve.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. For example:

| Criterion | Example standard |
|---|---|
| Correctness | Must preserve existing data and authentication behavior. |
| Effort | Should fit the available delivery and maintenance capacity. |
| Operational fit | Must work with current deployment, support, and ownership practices. |
| Reversibility | Should be removable or recoverable if it fails. |
| Verification | Must have a clear test or observable success condition. |

These criteria prevent the first plausible idea from winning by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variants of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer guidance, a process change, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an external service.

For highly ambiguous problems, generate a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, its major costs, and its key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate inputs and fail clearly for invalid states; do not silently turn programmer errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Place changes in the appropriate design boundary rather than applying a quick fix elsewhere.

## 6. Evaluate and recommend

Compare viable options against the criteria. Produce a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Store the proposal in the user’s chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear title, such as `DD MMM YYYY: Solve — [topic]`.

**Readiness gate:** Do not implement a hard-to-reverse commitment without an explicit decision. Do not proceed beyond this step for analysis-only work.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, dependencies, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm behavior against the evaluation criteria, including compatibility, failure behavior, and rollback assumptions.

**Verification audit:** Before claiming completion, confirm:

- The implemented behavior addresses the stated problem.
- Required tests and checks were run, with results recorded.
- Untested paths, assumptions, and known limitations are identified.
- No unapproved persistent interface, data, security, or vendor commitment was introduced.
- Release, commit, publication, and deployment actions follow the user’s established practices.

## 8. Hand off

Report the outcome in operational terms:

- What changed and what it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, monitoring, or rollback conditions.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and useful operational detail. Do not claim success solely because code was written or a configuration was changed.

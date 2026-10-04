---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only stopping point when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already clear. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the problem

Start with the underlying problem, not the user's proposed solution. If they ask to build a particular thing, work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would materially improve the situation?
- What constraints, permissions, security expectations, or compatibility requirements apply?

Write a concise problem statement and descriptive requirements. Describe the outcome and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so clearly.

Ask only for information that cannot be obtained from authorized, relevant documentation, code, systems, or prior project context. When reviewing private communications or records, confirm a legitimate purpose and clear authorization, use the minimum relevant information, and omit unrelated or sensitive personal details from notes and outputs.

## 2. Decide whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Treat “do nothing,” “deprioritize,” or “improve the current workaround” as real options.

Distinguish between:

- **Reversible decisions:** Small choices that are easy to change. Make a reasonable choice and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, migrations, public interfaces, long-lived settings, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the impact warrants it.

If direction or priority is unclear, present the tradeoff to the responsible decision-maker before investing in detailed design or implementation.

## 3. Research the current context

Read applicable project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and evidence from earlier attempts. Look for established patterns and reusable components before introducing new ones.

Understand deployment practices, ownership boundaries, supported environments, monitoring, data handling, and security expectations. Follow existing conventions unless there is a clear reason to change them.

## 4. Define evaluation criteria

Set explicit, lightweight criteria before generating solutions. For example:

- Must preserve current authentication, privacy, and data behavior.
- Must fit the available delivery time and maintenance capacity.
- Should avoid unnecessary dependencies and persistent configuration.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both selection and explanation. Without them, the first plausible option can win by accident.

## 5. Generate varied approaches

Generate genuinely different options, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code intervention, such as clearer instructions, a process change, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For highly ambiguous problems, generate a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate strictly and fail fast for invalid states. Do not hide programming errors by returning plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where practical.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is a stated requirement.
- Avoid quick fixes that bypass the appropriate design boundary.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

- Problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep proposals direct: usually one or two short paragraphs per option. Store durable proposals in the user's approved shared documentation system when review or collaboration is needed; otherwise provide them in the current workspace. Use a clear date-prefixed title, such as `04 Oct 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration and rollback strategy, test strategy, deployment steps, and ownership of follow-up actions. Keep the plan in a location where authorized reviewers can inspect and edit it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, and failure behavior.

Do not claim success based only on code changes. State what was tested, what passed, and what remains unverified. Commit, publish, or deploy only according to the user's repository, access-control, and release practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and useful operational detail. Do not include unrelated private information or expose material outside the intended access boundary.

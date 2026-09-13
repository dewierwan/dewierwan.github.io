---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to “build X,” work backward:

- Who experiences the problem, and in what role or situation?
- What are they trying to accomplish?
- What happens today?
- What workarounds exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the problem meaningfully better?

Write a concise problem statement and descriptive requirements. Describe the desired outcome, constraints, and success conditions rather than assuming a particular implementation.

If the proposed solution appears mismatched to the problem, say so directly. Ask only for information that cannot be found in authorized, relevant context such as project documentation, code, or operational records.

When using records or communications about people, confirm a legitimate purpose and clear authorization. Use the minimum relevant sources and details, omit unrelated sensitive information, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Include **do nothing**, **deprioritize**, or **improve the workaround** as real options when the issue is rare, low-cost, or adequately handled.

Distinguish between decisions that are easy to reverse and commitments that are expensive to undo:

- **Reversible decisions:** small choices with low switching cost. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** public interfaces, persistent data changes, migrations, long-lived settings, security boundaries, external contracts, or vendor commitments. Pause and obtain an explicit decision before implementing. Record the decision and rationale when appropriate.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing substantially in design or implementation.

## 3. Research the current context

Read the relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Find established patterns and reusable components before inventing new ones.

Understand compatibility requirements, deployment practices, access controls, supported environments, ownership boundaries, observability, and operational constraints. Follow the system’s conventions unless there is a clear reason to change them.

Research only sources needed for the problem. Do not copy personal details, credentials, internal identifiers, or unrelated operational information into proposals, plans, logs, or outputs.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, authorization, and data behavior.
- Must be feasible within the available time and maintenance capacity.
- Should avoid new dependencies, long-lived configuration, or permanent interfaces.
- Must have a clear verification method.
- Must be removable or reversible if it fails.
- Must meet relevant privacy, security, reliability, and performance requirements.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, training, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For an ambiguous problem, generate a wider set of candidates before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases whose behavior changes with runtime conditions.
- Validate inputs and invariants strictly. Fail clearly for invalid states rather than silently converting programming errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, integrations, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Put changes in the appropriate design boundary; avoid quick fixes that create hidden future work.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, dependencies, and open decisions.

Keep proposals direct and short: usually one or two paragraphs per option. Store durable proposals in the user’s chosen shared documentation system when review or collaboration is needed; otherwise provide them in the current workspace. Use a clear date-prefixed title, such as `13 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, data migration or rollback strategy, test strategy, deployment steps, and ownership of follow-up actions. Put the plan somewhere reviewers can inspect, edit, and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, access behavior, and failure behavior.

Do not claim success based only on implementation. State what was actually tested, the results, and what remains unverified. Commit, publish, or deploy changes only according to the user’s repository, review, and release practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Do not expose confidential information, personal details, credentials, or internal-only references beyond the audience’s authorized access boundary.

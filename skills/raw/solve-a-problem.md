---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, automation, or operational problem where the solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the problem

Start with the underlying problem, not the first solution suggested. If someone asks to “build X,” work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today?
- What workarounds or alternatives exist?
- How frequent, costly, urgent, or blocking is the problem?
- What outcome would make the situation meaningfully better?

Write a concise problem statement and descriptive requirements. Describe the desired outcome, constraints, and measures of success rather than assuming a particular implementation.

If a proposed solution does not appear to address the real problem, say so directly and explain why. Ask only for information that cannot be obtained from authorized, relevant documentation, code, records, or context.

When reviewing communications, operational records, or information about people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant sources and details, omit unrelated sensitive information, respect consent and privacy expectations, and keep findings within the appropriate access boundary.

## 2. Decide whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance cost. Treat “do nothing,” “deprioritize,” or “improve the current workaround” as real options when the issue is rare, low-cost, or adequately handled.

Distinguish between decision types:

- **Reversible decisions:** Small choices that are inexpensive to change. Make a reasonable choice and proceed.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, migrations, long-lived settings, security boundaries, external contracts, and vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the decision has lasting consequences.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in substantial design or implementation.

## 3. Research the current context

Read the relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operating procedures, and prior attempts. Look for established patterns and reusable components before inventing something new.

Understand compatibility requirements, deployment practices, supported environments, security expectations, ownership boundaries, monitoring, and rollback constraints. Use existing conventions unless there is a strong, stated reason to change them.

Research should answer:

- What already exists that could solve all or part of the problem?
- What has been attempted before, and what did it reveal?
- Which components, teams, systems, or policies would be affected?
- What assumptions need validation before design begins?

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve current authentication, authorization, and data behavior.
- Must fit the available delivery time and maintenance capacity.
- Should avoid unnecessary dependencies, configuration, or persistent state.
- Must have a clear verification method.
- Should be removable or reversible if it performs poorly.
- Must respect privacy, security, and applicable access boundaries.

These criteria guide both option generation and selection. Without them, the first plausible solution can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches rather than minor variations of one design. Consider:

1. Do nothing, defer, or improve the existing workaround.
2. A non-code solution, such as clearer instructions, a process adjustment, a template, training, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Building internally, purchasing a service, or integrating with an existing service.

For highly ambiguous or consequential problems, generate a broader set of candidates before narrowing. Keep each option short: what it is, what it solves, major costs, dependencies, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases whose behavior changes with runtime conditions.
- Validate inputs and invariants strictly. Fail visibly for invalid states rather than silently producing plausible but incorrect output.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Place changes in the appropriate design boundary; avoid expedient patches that create hidden coupling.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep proposals direct. A useful format is one or two short paragraphs per option, followed by a clear recommendation.

Store the proposal in the user’s chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear, date-prefixed title such as `07 Sep 2026: Solve — topic`.

**If this is analysis-only work, stop here.**

## 7. Plan, implement, and verify

For larger work, write an implementation plan before changing the system. Include:

- Scope and non-goals.
- Ordered implementation steps.
- Affected components and interfaces.
- Data migration, compatibility, rollback, and release strategy where relevant.
- Test strategy and acceptance checks.
- Deployment steps, monitoring, and owners of follow-up actions.

Keep the plan in a location where the appropriate reviewers can edit and approve it.

Implement the approved solution using the project’s conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, security, privacy, and failure behavior.

Do not claim success solely because code was written or a configuration was changed. State what was actually tested, the result, and what remains unverified. Commit, publish, or deploy only according to the user’s repository, release, and approval practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user action, rollout step, monitoring, or ownership.
- References to the proposal, plan, change set, or release record when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Do not bury the reader in temporary implementation notes.

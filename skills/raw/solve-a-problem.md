---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, recommendation, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to build a particular thing, work backward:

- Who experiences the problem and what are they trying to accomplish?
- What happens today, and what workarounds exist?
- How frequent, costly, urgent, or blocking is the problem?
- What outcome would make the situation meaningfully better?
- What constraints, dependencies, or boundaries matter?

Write a concise problem statement and descriptive requirements. Describe outcomes and constraints, not an assumed implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot be found in available project context, documentation, or authorized records. When accessing communications or records about people, confirm a legitimate purpose and clear authorization, use only the minimum relevant information, and omit unrelated or sensitive details from outputs.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, maintenance cost, and available alternatives. Treat “do nothing,” “deprioritize,” or improving a workaround as real options when the problem is low-impact or adequately handled.

Distinguish between:

- **Reversible decisions:** Small, easy-to-change choices. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived configuration, migrations, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation and record the rationale when appropriate.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in detailed design or implementation.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Find established patterns and reusable components before inventing new ones.

Understand compatibility requirements, deployment practices, access controls, supported environments, ownership boundaries, monitoring, and rollback expectations. Follow existing conventions unless there is a strong, documented reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, privacy, and data behavior.
- Must fit available time, budget, and maintenance capacity.
- Should avoid new dependencies, persistent settings, or public surface area.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

Criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For highly ambiguous problems, produce a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate strictly and fail clearly for invalid states. Do not hide programmer errors by returning plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Place changes in the appropriate design boundary rather than adding a quick fix in a convenient location.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep proposals direct and short. Store them in the user's chosen shared documentation system when durable review or collaboration is needed; otherwise provide them in the current workspace. Use a clear date-prefixed title, such as `02 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership. Keep the plan where appropriate reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, access boundaries, and expected failure behavior.

Do not claim success based only on implementation. State what was tested, what passed, and what remains unverified. Commit, publish, or deploy only according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.

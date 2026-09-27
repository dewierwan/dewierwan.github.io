---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff. The workflow supports analysis-only work when requested and emphasizes deliberate decisions.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, automation, or operational problem whose solution is not already obvious. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to "build X," work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including workarounds and failure points?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the situation meaningfully better?
- What constraints, such as timing, compatibility, security, or budget, apply?

Write a concise problem statement and descriptive requirements. Describe outcomes and constraints rather than assuming a particular implementation. If the proposed solution is poorly matched to the problem, say so directly.

Ask only for information that cannot be found in the available context, documentation, code, or authorized records. When consulting private communications or records about people, confirm a legitimate purpose and clear authorization; use only the minimum relevant information, omit unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Include “do nothing,” “defer,” or “improve the workaround” as real options when appropriate.

Distinguish decisions by reversibility:

- **Reversible decisions:** Small, easy-to-change choices. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived settings, migrations, security boundaries, vendor contracts, or externally visible commitments. Pause for an explicit decision before implementation. Record the decision and rationale when useful.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in substantial design or build work.

## 3. Research the current context

Read relevant project guidance, architecture notes, service documentation, code, tests, operational procedures, and prior attempts. Look for established patterns, reusable components, and existing platform capabilities before inventing something new.

Understand compatibility requirements, deployment and release practices, supported environments, ownership boundaries, security expectations, observability, and rollback options. Follow established conventions unless there is a strong, documented reason not to.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

| Criterion | Example standard |
|---|---|
| Compatibility | Must preserve existing authentication and data behavior. |
| Delivery effort | Must fit the available time and maintenance capacity. |
| Operational risk | Must have a clear verification and rollback method. |
| Long-term cost | Should avoid unnecessary dependencies, settings, and persistent surfaces. |

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change: clearer instructions, a process adjustment, a template, training, or an existing platform feature.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous problems, generate a broader candidate set before narrowing. Keep each option concise: what it is, which outcome it supports, principal costs, risks, and irreversible commitments.

### Design principles for technical options

- Prefer one understandable code path over special cases that vary by runtime conditions.
- Validate strictly and fail clearly for invalid states. Do not silently convert programmer errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, public interfaces, and contracts as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Put changes in the appropriate design boundary; do not rely on expedient patches that create hidden debt.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- Problem statement and current-state evidence.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, hard-to-reverse consequences, assumptions, and open decisions.

Store the proposal in the user's chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear, date-prefixed title such as `DD MMM YYYY: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, write an implementation plan before changing the system. Include scope, ordered steps, affected components, data migration or rollback strategy, test strategy, deployment steps, and ownership of follow-up actions. Keep the plan somewhere reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, permissions, privacy, and failure behavior.

Do not claim success based only on implementation. State what was actually tested, the observed result, and what remains unverified. Commit, publish, or deploy changes only according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, monitoring, or rollback triggers.
- References to the proposal, plan, and change set where applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.

---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, recommendation, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, automation, or operational problem where the solution is not already clear. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the problem

Start with the underlying problem, not the user’s proposed solution. If they ask to build something, work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today?
- What workarounds, failures, delays, or costs exist?
- How frequent, urgent, or blocking is the issue?
- What outcome would materially improve the situation?

Write a concise problem statement and descriptive requirements. State the desired outcome and constraints, not a presumed implementation. If the proposed solution does not appear to solve the stated problem, say so directly.

Ask only for information that cannot be found in authorized, relevant context. When reviewing communications, records, or user data, confirm a legitimate purpose and clear authorization; use the minimum relevant sources and omit unrelated or sensitive personal details.

## 2. Decide whether to solve it now

Assess severity, frequency, affected users, opportunity cost, existing alternatives, and maintenance burden. Treat **do nothing**, **deprioritize**, or **improve the current workaround** as valid options when the problem is low-impact or adequately handled.

Separate decisions by reversibility:

- **Reversible decisions:** small choices that are easy to change. Use reasonable judgment, choose, and proceed.
- **Hard-to-reverse decisions:** persistent data changes, migrations, public interfaces, long-lived configuration, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the commitment warrants it.

If priority or direction is unclear, present the tradeoff to the responsible decision-maker before investing heavily in design or implementation.

## 3. Research the current context

Read the relevant project guidance, architecture notes, repository documentation, existing code, tests, operating procedures, and prior attempts. Find established patterns, reusable components, and constraints before inventing something new.

Understand compatibility, deployment, security, ownership, monitoring, supported environments, and access boundaries. Follow the system’s established conventions unless there is a strong, documented reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, permissions, and data behavior.
- Must fit the available delivery time and maintenance capacity.
- Should avoid new dependencies and long-lived configuration.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

Without criteria, the first plausible approach can win by accident.

## 5. Generate varied approaches

Generate genuinely different options, not minor variations of the same design. Consider:

1. Do nothing, defer, or improve the workaround.
2. A non-code solution: clearer guidance, a process adjustment, a template, or an existing platform capability.
3. A small, targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For a highly ambiguous problem, generate a broader candidate set before narrowing. Describe each option briefly: what it is, what it solves, major costs, and key risks.

### Technical design principles

- Prefer one understandable code path over runtime-specific special cases.
- Validate strictly and fail fast for invalid states; do not silently turn programming errors into plausible but wrong results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer bounded changes that can be deleted or rolled back cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Place changes in the appropriate design boundary; do not use a quick fix that creates hidden future cost.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

| Section | Required content |
|---|---|
| Problem | Concise problem statement and desired outcome. |
| Criteria | The evaluation criteria used to compare options. |
| Options | Viable approaches with meaningful tradeoffs. |
| Recommendation | One clear recommendation and why it is preferred. |
| Decisions and risks | Important open questions, irreversible consequences, and mitigations. |

Keep proposals direct. Store a durable proposal in the user’s chosen shared documentation system when review, approval, or collaboration requires it; otherwise provide it in the current workspace. Use a clear date-prefixed title, such as `14 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, verify, and hand off

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration and rollback strategy, test strategy, deployment steps, and follow-up ownership. Put the plan where relevant reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Check the result against the evaluation criteria, including compatibility, permissions, failure behavior, and rollback expectations.

Do not claim success based only on completed code or configuration. State what was tested, what passed, and what remains unverified. Commit, publish, or deploy only according to the user’s repository and release practices.

Finish with a focused handoff:

- What changed and the user outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required rollout, monitoring, or user actions.
- Links or references to the proposal, plan, and change set when applicable.

## Readiness and audit checks

Before recommending: confirm the problem statement, criteria, alternatives, recommendation, and hard-to-reverse decisions are clear.

Before implementing: confirm authorization, scope, approval for consequential commitments, and a verification plan.

Before handoff: confirm outputs remain within the appropriate access boundary, sensitive details are excluded unless necessary and authorized, and success claims match actual evidence.

Common failure modes are implementing the first requested solution without diagnosing the problem, adding permanent configuration for a temporary need, silently hiding invalid states, treating a hard-to-reverse commitment as routine work, and reporting completion without meaningful verification.

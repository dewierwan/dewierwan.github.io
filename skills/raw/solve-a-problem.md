---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only stopping point when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already clear. Do not use it for a small fix, a routine task with a known implementation, or a request that only needs a direct answer.

By default, work from understanding through implementation and handoff. If the user requests analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the problem

Start with the underlying problem rather than the user's proposed solution. If the request is "build X," work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today?
- What workarounds, failures, delays, or risks exist?
- How frequent, urgent, costly, or blocking is the problem?
- What outcome would meaningfully improve the situation?

Write a concise problem statement and descriptive requirements. State the desired outcome, constraints, and success conditions without assuming a particular implementation.

If the proposed solution does not appear to address the actual problem, say so plainly and explain why. Ask only for information that cannot reasonably be learned from authorized project context, documentation, code, or records.

When reviewing private communications, operational records, or information about people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant sources, omit unrelated personal details, and keep findings within the appropriate access boundary.

## 2. Assess priority and decision readiness

Decide whether this should be solved now. Consider severity, frequency, number of affected users, opportunity cost, available workarounds, and maintenance cost. Treat “do nothing,” “deprioritize,” or “improve the workaround” as valid options.

Classify the decision:

- **Reversible decision:** A small choice that can be changed cheaply. Use reasonable judgment, choose, and proceed.
- **Hard-to-reverse decision:** A public interface, persistent data change, migration, long-lived setting, security boundary, external contract, or vendor commitment. Pause before implementation and obtain an explicit decision from the responsible owner.

If priority or direction is unclear, present the tradeoff before investing in detailed design. Record the rationale for consequential decisions when useful.

**Readiness gate:** Proceed to solution design only when the problem, owner, desired outcome, and decision authority are sufficiently clear. Otherwise, return with focused questions or recommend discovery work.

## 3. Research the current context

Review the relevant project guidance, architecture notes, service documentation, existing code, tests, operational procedures, prior attempts, and known constraints. Look for established patterns, reusable components, and existing platform capabilities before creating something new.

Check compatibility requirements, deployment and release practices, data handling rules, supported environments, ownership boundaries, monitoring, and security expectations. Follow existing conventions unless there is a strong, documented reason not to.

Keep a distinction between facts, assumptions, and unknowns:

| Type | Example |
|---|---|
| Fact | Existing authentication must remain compatible. |
| Assumption | Most users can complete the workflow without training. |
| Unknown | Expected peak request volume has not been confirmed. |

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. Adapt these to the problem:

- Must preserve important existing behavior, including authorization and data integrity.
- Must fit the available delivery time and maintenance capacity.
- Should avoid unnecessary dependencies, services, persistent settings, and public surface area.
- Must have a clear test and verification method.
- Should be reversible or removable if it fails.
- Must meet applicable privacy, security, reliability, and accessibility requirements.

These criteria prevent the first plausible solution from winning by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change: clearer instructions, a process change, a template, training, or use of an existing capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For an ambiguous or high-impact problem, expand the candidate set before narrowing. Keep each option concise: what it is, what it solves, major costs, important risks, and reversibility.

### Technical design principles

- Prefer one understandable execution path over special cases that vary by runtime condition.
- Validate inputs and invariants strictly. Fail clearly when an invalid state indicates a defect; do not silently convert bugs into plausible output.
- Prefer established conventions over new abstractions, and new abstractions over permanent configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed without widespread entanglement.
- Use familiar, proven technology and existing infrastructure unless a new tool clearly earns its cost.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is a stated requirement.
- Avoid quick fixes that bypass the appropriate system boundary.

## 6. Evaluate and recommend

Compare viable options against the criteria. Provide a concise proposal with:

- Problem statement and current impact.
- Evaluation criteria.
- Options and material tradeoffs.
- One clear recommendation and why it is preferred.
- Key risks, assumptions, irreversible consequences, and open decisions.

Use a durable shared documentation system when review, approval, or future reference is needed; otherwise use the current workspace. Use a clear title such as `DD MMM YYYY: Solve — [topic]`.

**Recommendation gate:** Do not implement a hard-to-reverse choice without explicit approval. If the user requested analysis only, stop here.

## 7. Plan, implement, and verify

For larger work, prepare an implementation plan before changing the system. Include scope, ordered steps, affected components, dependencies, migration or rollback strategy, test strategy, release steps, monitoring, and follow-up ownership.

Implement the approved solution using the project's conventions. Run relevant automated tests, static checks, and focused manual verification. Verify both normal behavior and meaningful failure behavior.

### Completion audit

Before declaring completion, check:

- The delivered behavior addresses the stated problem and evaluation criteria.
- Existing critical behavior remains compatible.
- Tests and checks actually ran; report their results accurately.
- Errors are visible and actionable rather than silently masked.
- Security, privacy, and access boundaries remain appropriate.
- Rollback, removal, or operational recovery is understood where relevant.

Do not claim success based solely on code changes or a successful build.

## 8. Hand off

Report the outcome in operationally useful terms:

- What changed and what user outcome it enables.
- Verification performed, results, and anything not verified.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change record when applicable.

Keep the handoff focused. Separate confirmed results from assumptions, and state clearly if implementation is blocked pending a decision, authorization, or missing information.

---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only stopping point when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already clear. Do not use it for a small fix or routine task with a known implementation path.

By default, work end-to-end. If the requester says not to implement yet, or asks for analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the actual problem

Start with the outcome needed, not the first solution proposed. If someone asks to build a feature, work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today?
- What workaround, if any, exists?
- How often does it happen, how severe is it, and what does it block?
- What would a successful outcome look like?
- What constraints matter: time, budget, compatibility, security, privacy, operations, or maintainability?

Write a concise problem statement and descriptive requirements. Describe the required result rather than assuming a particular technology or design. If the proposed solution does not match the problem, say so plainly.

Ask only for information that cannot be learned from authorized, relevant context such as project documentation, code, tests, or process records. When reviewing private communications or records, confirm a legitimate purpose and authorization, use the minimum relevant material, and exclude unrelated or sensitive personal information.

## 2. Decide whether to act now

Assess severity, frequency, affected users, alternatives, opportunity cost, and urgency. Treat **do nothing**, **deprioritize**, or **improve the workaround** as real options when the problem is low impact or adequately handled already.

Separate decisions by reversibility:

- **Reversible decisions:** Small choices that are cheap to change. Make a reasonable choice and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, migrations, public interfaces, long-lived settings, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the commitment is material.

If direction or priority is unresolved, present the tradeoff to the responsible decision-maker before spending substantial effort on detailed design or implementation.

## 3. Research the current context

Read relevant repository instructions, architecture notes, service documentation, code, tests, operational runbooks, and records of prior attempts. Identify existing patterns, shared components, and project conventions before proposing new abstractions.

Check practical constraints: supported environments, deployment and rollback practices, access boundaries, dependency policy, monitoring, ownership, performance expectations, and compatibility requirements. Prefer the existing system's conventions unless there is a strong, stated reason to depart from them.

## 4. Define evaluation criteria

Set explicit criteria before generating options. Keep them proportionate to the problem. Typical criteria include:

- Preserves existing behavior, access controls, and data integrity.
- Fits available engineering and maintenance capacity.
- Avoids unnecessary dependencies and permanent configuration.
- Has a clear, realistic test and verification method.
- Can be removed, rolled back, or contained if it fails.
- Meets stated performance, reliability, or delivery constraints.

These criteria prevent the first plausible solution from winning by default.

## 5. Generate varied approaches

Create genuinely different options, not minor variants of one design. Consider:

1. Do nothing, defer, or improve the existing workaround.
2. A non-code solution: guidance, process change, template, training, or an existing platform capability.
3. A small, targeted technical change.
4. A broader integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous or high-impact problems, generate a wider candidate set before narrowing. For each option, state what it is, the expected outcome, main costs, risks, and irreversible consequences.

### Design rules for technical options

- Prefer one understandable execution path over runtime-specific special cases.
- Validate inputs and invariants strictly. Fail visibly for invalid states rather than silently producing plausible but incorrect output.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new data fields, settings, and public interfaces as maintenance commitments.
- Favor bounded, loosely coupled changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure when suitable.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is a stated requirement.
- Place changes in the appropriate design boundary; do not use a quick workaround that creates lasting structural debt.

## 6. Evaluate and recommend

Compare viable options against the criteria. Produce a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Options and their tradeoffs.
- One clear recommendation and why it best fits the criteria.
- Key risks, hard-to-reverse consequences, assumptions, and open decisions.

Use a shared documentation location selected by the requester when review, editing, or durable decision records are needed. Otherwise, provide the proposal in the agreed workspace. Use a clear date-prefixed title, such as `19 Sep 2026: Solve — topic`.

**Analysis-only gate:** If implementation is not authorized, stop here. Do not begin changes merely because a recommendation has been made.

## 7. Plan, implement, and verify

For larger work, prepare an implementation plan before making changes. Include scope, ordered steps, affected components, dependencies, migration and rollback approach, test strategy, deployment steps, and follow-up ownership. Put the plan where relevant reviewers can inspect and edit it.

Implement the approved approach using project conventions. Run relevant automated tests, static checks, and focused manual verification. Test expected behavior, important failure modes, access boundaries, compatibility, and rollback assumptions where applicable.

Audit before declaring success:

- Does the delivered change solve the stated problem rather than merely match the original suggestion?
- Does it meet the evaluation criteria?
- Were irreversible changes explicitly approved?
- Are failures visible and diagnosable rather than silently masked?
- Is the change appropriately bounded, testable, and maintainable?
- What was actually verified, and what remains unverified?

Do not claim success based only on code being written. Commit, publish, deploy, or otherwise release changes only through the user's authorized repository and release practices.

## 8. Hand off

Report the outcome in operational terms:

- What changed and what it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required rollout, user action, monitoring, or ownership follow-up.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused and direct. Surface failure modes and unresolved decisions rather than burying them in implementation detail.

---
name: solve-a-problem
description: Take a non-trivial problem from diagnosis through recommendation, implementation, verification, and handoff, with a clear analysis-only stopping point.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, or automation problem where the right solution is not yet clear. Do not use it for small fixes or routine tasks with a known implementation.

By default, work from understanding through implementation and handoff. If the user requests analysis only, stop after the recommendation and wait for an explicit decision.

## Entry and decision gate

Enter this workflow when there is a committed problem worth exploring, but the implementation is unclear. If the underlying problem, priority, or strategic direction is still disputed, first use a suitable discovery, challenge, or decision process rather than designing prematurely.

Before implementation, classify the main decision:

- **Reversible:** A small, cheap-to-change choice. Make a reasonable choice, state the assumption, and proceed.
- **Hard to reverse:** A persistent data change, public interface, long-lived setting, migration, security boundary, external contract, or vendor commitment. Pause for an explicit decision before implementation. Record the rationale, owner, alternatives, and consequences when the commitment warrants it.

Do not hide a hard-to-reverse commitment inside an otherwise ordinary implementation task.

## 1. Understand the problem

Start with the underlying problem, not the first proposed solution. If someone asks to “build X,” work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today?
- What workarounds, delays, failures, or risks exist?
- How frequent and how blocking is the problem?
- What outcome would materially improve the situation?

Write a concise problem statement and descriptive requirements. Describe desired outcomes and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot reasonably be found in available documentation, code, approved records, or system context.

### Boundaries for people-related information

If the work requires communications, records, or other information about identifiable people, establish a legitimate stated purpose and clear authorization first. Review only the minimum relevant sources, time range, fields, and excerpts. Omit unrelated personal or sensitive details, respect consent and confidentiality expectations, and keep notes and outputs within the approved audience.

When authority, consent, or permitted use is unclear, pause and ask the responsible owner. Prefer anonymized or aggregated evidence when it supports the decision equally well.

## 2. Decide whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and ongoing maintenance burden. Treat “do nothing,” “deprioritize,” and “improve the current workaround” as real options.

If priority or direction is unclear, present the tradeoff to the responsible decision-maker before investing substantially in design or implementation.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Find established patterns, reusable components, and existing platform capabilities before creating something new.

Identify compatibility, deployment, access-control, privacy, supported-environment, ownership, monitoring, and rollback constraints. Follow existing conventions unless there is a strong documented reason to depart from them.

For sensitive research, retain only an appropriate audit record: purpose, authorizing role, sources reviewed, scope, and access restrictions. Do not copy source material into working notes unless necessary.

## 4. Define evaluation criteria

Set explicit, lightweight criteria before generating solutions. At minimum, cover:

- Required user outcome and compatibility constraints.
- Delivery effort and ongoing maintenance capacity.
- Operational risk, rollback, or containment path.
- Simplicity, including avoidance of unnecessary dependencies and permanent settings.
- Verification method and expected failure behavior.
- Privacy and access boundaries where data about people is involved.

These criteria prevent the first plausible option from winning by accident.

## 5. Generate varied approaches

Generate genuinely different options, not minor variants of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer guidance, a process adjustment, a template, or an existing platform feature.
3. A small targeted technical change.
4. A larger integrated solution.
5. Building, buying, or integrating an existing service.

For highly ambiguous work, generate a wider set before narrowing. Keep each approach to one or two short paragraphs: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate inputs and fail clearly for invalid states. Do not hide programming errors behind plausible fallback results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer bounded changes that can be removed without widespread entanglement.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is a stated requirement.
- Put changes in the appropriate design boundary; avoid quick fixes that create future maintenance problems.
- Collect, expose, retain, and transmit only data necessary for the approved purpose.

## 6. Evaluate and recommend

Compare viable options against the criteria. Use this proposal format:

```text
Title: DD MMM YYYY: Solve — [topic]

Problem
[One concise statement of the user outcome, current gap, and constraints.]

Criteria
[The criteria used to compare options.]

Options
1. [Option]: [benefit, cost, and key risk.]
2. [Option]: [benefit, cost, and key risk.]

Recommendation
[One recommended option and why it best meets the criteria.]

Decision needed
[Owner, hard-to-reverse commitments, open questions, and approval needed.]

Risks and verification
[Main risks, rollback or containment approach, and how success will be checked.]
```

Keep the proposal direct and concise. Store it in the user’s approved shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Share it only with people authorized to receive its content.

**Analysis-only gate:** If analysis-only was requested, stop here. Do not create an implementation plan, change systems, or imply approval to proceed.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, data or migration needs, rollback strategy, test approach, deployment steps, and follow-up ownership.

Before implementation, confirm this readiness gate:

- The recommendation or chosen direction is approved by the appropriate owner.
- Any hard-to-reverse decision is explicit and documented.
- Required access, privacy, and security approvals are in place.
- Success criteria, test method, rollout path, and rollback or containment path are known.
- The implementation scope has a clear boundary and owner.

Implement using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, authorization, privacy, and expected failure behavior.

Before release, check that the solution enforces its intended access boundary, does not expose sensitive information through logs or shared artifacts, uses authorized test data, and has appropriate retention or deletion behavior for stored data.

Do not claim success based only on completed code. State what was tested, the results, and what remains unverified. Commit, publish, or deploy only according to the user’s repository and release practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, monitoring, and ownership.
- Any continuing access, consent, retention, or privacy obligations.
- References to the proposal, plan, and change set where applicable.

Keep the handoff focused on operationally useful outcomes. Share technical and operational detail only with the approved audience, and exclude unnecessary personal or sensitive information.

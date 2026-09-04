---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, recommendation, implementation, verification, and handoff. Supports analysis-only work when the user asks not to implement yet.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already clear. Do not use it for a small fix or routine task with a known implementation.

By default, proceed from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the underlying problem

Start with the problem, not the requested solution. If the request is “build X,” work backward:

- Who is affected, and what are they trying to accomplish?
- What happens now, including workarounds?
- How often does it occur, and how severe, costly, urgent, or blocking is it?
- What outcome would materially improve the situation?
- What constraints are already known: time, security, compatibility, budget, ownership, or access?

Write a concise problem statement and descriptive requirements. State outcomes and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so clearly.

### Rules for people-related information

If understanding the problem requires reviewing communications, records, analytics, or other information about people:

1. Establish and state the legitimate purpose before accessing or analyzing the information.
2. Confirm clear authorization for the specific sources, people, and use. Do not infer authorization from general system access.
3. Use only the minimum relevant sources, date range, fields, and excerpts needed to answer the problem.
4. Do not collect, repeat, or expose unrelated personal information or sensitive information, such as health, financial, identity, family, private communications, or protected characteristics, unless it is necessary, authorized, and lawful to use.
5. Respect applicable consent, notice, retention, confidentiality, and privacy expectations. If consent or expected use is unclear, pause and seek clarification.
6. Keep notes, proposals, and outputs within the authorized audience and access boundary. Prefer aggregated, de-identified, or role-level findings when they answer the question.

Do not use people-related information for a purpose beyond the stated problem, and do not make claims about an individual that are unsupported by relevant evidence.

## 2. Check priority and decision readiness

Assess whether this is worth solving now. Consider severity, frequency, people affected, available workarounds, opportunity cost, and the cost of delay. “Do nothing,” “defer,” or “improve the workaround” must remain real options.

Classify decisions:

- **Reversible:** Small choices that can be changed cheaply. Use reasonable judgment and proceed.
- **Hard to reverse:** Public interfaces, persistent data changes, migrations, long-lived settings, security boundaries, vendor commitments, or external contracts. Pause for an explicit decision before implementation.

If direction, ownership, priority, or authority is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design work. Record rationale for consequential decisions when useful.

**Readiness gate:** Do not design a committed solution until the problem, priority, decision owner, authority to proceed, and any required data-access authorization are sufficiently clear.

## 3. Research current context

Inspect relevant project guidance, architecture notes, repository documentation, existing code, tests, operational procedures, service documentation, and prior attempts. Look for established patterns and reusable components before creating new ones.

Identify compatibility requirements, deployment practices, security expectations, supported environments, data flows, ownership boundaries, observability, and rollback limits. Use existing conventions unless there is a strong, documented reason not to.

When research involves people-related data, record the authorized purpose, sources used, and access limits. Avoid copying raw records into broadly shared documents. Redact or omit personal and sensitive details unless their inclusion is necessary and authorized for the intended audience.

## 4. Define evaluation criteria

Define explicit criteria before selecting an approach.

| Criterion | Example threshold or question |
|---|---|
| Correctness | Does it preserve required behavior and data integrity? |
| Safety and privacy | Does it maintain authorization, consent expectations, confidentiality, and minimum-necessary data use? |
| Effort | Is it feasible within available delivery and maintenance capacity? |
| Reversibility | Can it be removed or rolled back safely? |
| Verification | Can success and failure behavior be tested clearly? |

Add problem-specific criteria such as latency, accessibility, reliability, cost, or operational burden. These criteria prevent the first plausible idea from winning by accident.

## 5. Generate varied approaches

Generate genuinely different options, not minor variations. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution: instructions, training, process changes, templates, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous or high-impact work, produce a wider candidate set before narrowing. Describe each viable option briefly: what it is, what it solves, main costs, risks, data implications, and irreversible commitments.

### Technical design rules

- Prefer one understandable code path over runtime-specific special cases.
- Validate strictly and fail visibly for invalid states; do not silently turn programming errors into plausible results.
- Prefer established conventions over new abstractions, and abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer bounded changes that can be removed cleanly.
- Use proven technology and existing infrastructure unless a new choice has a clear advantage.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Avoid quick fixes outside the appropriate design boundary.

## 6. Evaluate and recommend

Compare options against the criteria. Provide a short proposal with:

- Problem statement and current-state evidence.
- Evaluation criteria.
- Viable options and key tradeoffs.
- One clear recommendation and why it is preferred.
- Risks, irreversible effects, assumptions, data-handling implications, and open decisions.

Store durable proposals in the user’s chosen shared documentation system when review or collaboration is needed; otherwise use the current workspace. Apply access controls appropriate to the proposal’s contents. Do not place personal or sensitive source material in a document shared beyond the authorized audience. Use a clear date-prefixed title, such as `04 Sep 2026: Solve — topic`.

**Analysis-only gate:** If implementation was not requested, stop here. Do not make changes merely because a recommendation exists.

## 7. Plan, implement, and verify

For larger work, create a reviewable implementation plan covering scope, ordered steps, affected components, data migration and rollback, tests, deployment, monitoring, and follow-up ownership. Obtain required approval before crossing hard-to-reverse boundaries.

Implement using project conventions. Run relevant tests, static checks, and focused manual verification. Test normal behavior, important failure behavior, compatibility, authorization boundaries, and rollback or recovery where applicable.

If the solution processes information about people, verify that it enforces the approved purpose, least-privilege access, minimum necessary collection and retention, sensitive-data protections, consent or notice requirements where applicable, and output access controls. Test that unauthorized users cannot retrieve records, inferences, or exports.

Audit before declaring completion:

- Does the result meet each evaluation criterion?
- Were authorized sources and the minimum necessary information used?
- Were personal or sensitive details omitted, protected, or restricted to the authorized audience?
- Were tests actually run, and what did they show?
- Are migrations, releases, or external changes reversible or explicitly accepted?
- Are known limitations and unverified assumptions recorded?

Do not claim success based solely on completed code. Commit, publish, or deploy only under the user’s repository and release practices.

## 8. Hand off

Report the user outcome, what changed, verification performed and results, known limitations, deferred work, rollout or monitoring needs, and any required user action. Include links or references to the proposal, plan, and change record when applicable.

Share the handoff only with people authorized to receive it. Use concise, audience-appropriate detail; provide de-identified summaries where possible and avoid including raw personal records, sensitive details, credentials, or unnecessary internal implementation data.

Common failure modes are implementing the initial request without diagnosing the need, treating an irreversible commitment as routine, selecting the first plausible option without criteria, adding permanent configuration for a temporary case, hiding defects through broad error handling, using people-related data without a clear purpose or authorization, collecting more personal data than needed, exposing sensitive details to an overly broad audience, and reporting completion without evidence of verification.

---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only mode.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, automation, integration, or operational problem where the right solution is not already clear. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start from the underlying problem, not the first proposed solution. When someone asks to “build X,” work backward:

- Who is affected and what are they trying to accomplish?
- What happens today?
- What workarounds or alternatives exist?
- How frequent, costly, urgent, or blocking is the issue?
- What outcome would make the situation meaningfully better?

Write a concise problem statement and descriptive requirements. Define the desired outcome, constraints, and measures of success without assuming a particular implementation. If the proposed solution does not fit the problem, say so clearly.

Ask only for information that cannot be found in available documentation, code, approved records, or the user’s supplied context.

### Boundaries for people-related information

If understanding the problem requires reviewing communications, support cases, employee records, customer records, usage data, or other information about people:

- Establish a legitimate, specific purpose for the review.
- Confirm that the requester has clear authorization to access the sources and use them for this purpose.
- Use the minimum sources, date range, fields, and excerpts needed to answer the question.
- Respect applicable consent, notice, confidentiality, retention, and privacy expectations. Do not assume that access to a system authorizes a new use of its contents.
- Avoid collecting or repeating sensitive personal information unless it is necessary for the stated purpose and appropriately authorized. Sensitive information may include health, financial, identity, precise location, legal, family, demographic, or private communication details.
- Remove names, identifiers, and unnecessary personal details from working notes and outputs where possible. Prefer aggregated or anonymized findings.
- Keep outputs within the appropriate access boundary. Share findings only with people authorized to receive them, and do not move sensitive material into broader documentation, tickets, logs, or public channels.

If authorization, purpose, consent expectations, or the safe output audience is unclear, pause and ask for clarification before reviewing or disclosing the information.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, existing alternatives, and maintenance burden. “Do nothing,” “deprioritize,” or “improve the current workaround” are valid options when the problem is low impact or already adequately handled.

Distinguish between:

- **Reversible decisions:** Small choices that are inexpensive to change. Use reasonable judgment and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, migrations, public interfaces, long-lived configuration, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation.

If priority or direction is unclear, present the tradeoff and ask the accountable decision-maker to choose before investing in detailed design or implementation. Record consequential decisions and their rationale when useful.

## 3. Research the current context

Read the relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operating procedures, and previous attempts. Find established patterns and reusable components before creating new ones.

Understand compatibility requirements, deployment practices, supported environments, access boundaries, security expectations, ownership, observability, and rollback constraints. Follow existing conventions unless there is a clear reason to change them.

When research involves restricted systems or people-related records, document the purpose, authorized sources, and intended audience at a level appropriate to the work. Do not copy raw sensitive content into proposals or implementation plans unless it is necessary, authorized, and access-controlled.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. For example:

| Criterion | Example expectation |
|---|---|
| Compatibility | Must preserve current authentication and data behavior. |
| Delivery | Should fit the available time and maintenance capacity. |
| Operational cost | Prefer no new dependency or long-lived configuration. |
| Quality | Must have a practical verification method. |
| Reversibility | Should be removable or recoverable if it fails. |
| Data handling | Must use only authorized data and keep outputs within the intended access boundary. |

These criteria guide both solution generation and selection. Without them, the first plausible approach can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, rather than small variations of one design. Always consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer guidance, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For especially ambiguous problems, generate a wider set of candidates before narrowing. Keep each option concise: what it is, what it solves, main costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate strictly and fail fast for invalid states. Do not silently transform programming errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer loosely coupled, well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure when suitable.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Avoid quick fixes that bypass the appropriate design boundary.
- For systems handling people-related information, minimize collection, restrict access, avoid unnecessary retention, and make authorization boundaries enforceable rather than relying only on policy.

## 6. Evaluate and recommend

Compare viable options against the evaluation criteria. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.
- For people-data work, the legitimate purpose, authorized information scope, sensitive-data safeguards, consent or notice considerations, and intended output audience.

Keep proposals direct and brief. Store durable proposals in the user’s chosen shared documentation system when review or collaboration is needed; otherwise provide them in the current workspace. Use a clear date-prefixed title, such as `DD MMM YYYY: Solve — topic`.

Do not include raw private communications, unnecessary identifiers, or sensitive details in a broadly accessible proposal. Use summaries, aggregates, redaction, or a restricted appendix where needed. Confirm that proposal access matches the authorization boundary before sharing it.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, access and data handling, migration and rollback strategy, test strategy, deployment steps, and follow-up ownership.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm results against the evaluation criteria, including compatibility, privacy, security, authorization, and failure behavior.

If the implementation accesses or processes people-related data, verify that:

- Access is limited to authorized roles and systems.
- The solution collects and retains only necessary information.
- Sensitive values are protected in interfaces, logs, test fixtures, analytics, and error reporting.
- Consent, notice, and user-control requirements are met where applicable.
- Outputs, exports, alerts, and dashboards are available only to appropriate audiences.
- Test data is synthetic or otherwise approved for testing.

Do not claim success solely because code was written. State what was tested, the results, and what remains unverified. Commit, publish, or deploy only according to the user’s repository and release practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.
- Any continuing access, consent, retention, or output-sharing constraints relevant to the solution.

Keep the handoff focused on outcomes and operationally useful detail. Share it only through channels suitable for its information sensitivity, and avoid burying the reader in temporary implementation notes.

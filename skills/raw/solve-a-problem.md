---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's proposed solution. If they ask to build something, work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, and what workarounds exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the situation meaningfully better?

Write a concise problem statement and descriptive requirements. Describe outcomes and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot be found in available project context, documentation, or authorized records. When reviewing communications or records about people, confirm a legitimate purpose and clear authorization, use only the minimum relevant material, and omit unrelated or sensitive personal details.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Treat “do nothing,” “deprioritize,” or “improve the workaround” as valid options when the issue is low impact or adequately handled already.

Distinguish between:

- **Reversible decisions:** Small choices that are cheap to change. Make a reasonable choice and move forward.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived settings, migrations, security boundaries, external contracts, or vendor commitments. Pause for explicit approval before implementation, and record the rationale when appropriate.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in detailed design or implementation.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operating procedures, and prior attempts. Look for established patterns, reusable components, and constraints before inventing a new approach.

Understand compatibility requirements, deployment practices, access boundaries, security expectations, supported environments, ownership, monitoring, and rollback capabilities. Use the system’s existing conventions unless there is a clear reason not to.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, privacy, and data behavior.
- Must fit available delivery time and ongoing maintenance capacity.
- Should avoid unnecessary dependencies, public interfaces, or permanent configuration.
- Must have a clear verification method.
- Should be removable, reversible, or safely recoverable if it fails.

These criteria guide option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For especially ambiguous problems, generate a wider set of candidates before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-specific special cases.
- Validate inputs and states strictly. Fail loudly for programmer errors rather than silently producing plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Put changes in the appropriate design boundary; avoid expedient fixes that create future confusion.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep proposals direct and brief. Store them in the user’s chosen shared documentation system when durable review or collaboration is needed; otherwise provide them in the current workspace. Use a clear, date-prefixed title, such as `DD MMM YYYY: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, access or data changes, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership. Put the plan somewhere reviewers can edit and approve it.

Implement the approved solution using project conventions and authorized access only. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy expectations, and failure behavior.

Do not claim success based only on implementation. State what was tested, the results, and what remains unverified. Commit, publish, or deploy changes only according to the user’s repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.

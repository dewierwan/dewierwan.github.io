---
name: solve-a-problem
description: Takes a non-trivial build or process problem from diagnosis to options, recommendation, and implementation. Use when someone says "build X" or "think it through, don't build yet".
---

# Solve a problem

Use this workflow to take a non-trivial build, integration, automation, process, or operational problem from understanding through options, a clear recommendation, implementation, and verification. It is meant for problems where the shape of the solution is not obvious, not for small fixes or routine tasks with a known implementation.

## Quick version

- Restate the underlying problem in your own words before discussing solutions: who is affected, what they are trying to do, what happens today, and how much it hurts. If the requested solution does not fit the problem, say so.
- Decide whether it is worth solving now, and flag any hard-to-reverse choices (data changes, public interfaces, long-lived settings, vendor commitments) for an explicit decision first.
- Write three to five lightweight evaluation criteria before generating ideas.
- Generate genuinely different options, always including "do nothing or defer" and a non-code option, plus small and larger technical versions.
- Compare options against the criteria in a short table and make one clear recommendation with reasons. Give it directly in the reply.
- If the user asked for analysis only, stop there. Otherwise plan, implement, verify, and report what was tested and what was not.

## When to use it

By default, work from understanding all the way through implementation. If the user says something like "just think this through, don't build yet," stop after the recommendation in Step 6 and wait for a decision.

Enter this workflow when the direction is already committed. If the user is still exploring what to do at all, first generate ideas, stress-test them, and make the decision, then come back here.

## 1. Understand the problem

Start with the underlying problem, not the user's proposed solution. If they ask to build something, work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is the problem?
- What outcome would make the situation meaningfully better?
- What constraints, dependencies, deadlines, or access boundaries apply?

Write a concise problem statement and descriptive requirements. Describe the desired outcome and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so directly at this stage rather than building it and hoping.

Ask only for information that cannot be found in available project context, documentation, code, or records.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Include "do nothing," "deprioritize," or "improve the current workaround" as real options when appropriate.

Separate decisions by reversibility:

- **Reversible decisions:** Small choices that are easy to change. Use reasonable judgment, choose, and move forward without agonizing.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived configuration, security boundaries, migrations, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the decision and rationale when the consequence warrants it. Do not quietly build a hard-to-reverse commitment inside an implementation task.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before creating new ones.

Identify constraints such as compatibility requirements, deployment practices, ownership boundaries, supported environments, security expectations, observability, and rollback needs. Use established system conventions unless there is a clear reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. For example:

- Must preserve existing authentication, privacy, and data behavior.
- Must fit available time, skills, and maintenance capacity (set the time budget that fits your situation).
- Should avoid new dependencies, persistent settings, and public surface area.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not small variations of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer instructions, a process adjustment, a template, a better-organized view in an existing tool, a no-code automation, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Building, buying, or integrating an existing service.

For ambiguous or complex problems, generate a wider set of candidates before narrowing. Keep each option short: one or two brief paragraphs covering what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- **One code path over special cases.** A single path is easier to reason about, test, and debug, even if slightly less efficient.
- **Fail clearly on invalid states.** Validate inputs and use strict types. Do not hide programming errors by silently producing plausible but incorrect output.
- **Convention over composability over configuration.** Prefer established patterns, then flexible abstractions, and only then config-driven behavior.
- **Avoid permanent commitments.** New fields, settings, and public interfaces must be maintained indefinitely; treat them as hard-to-reverse decisions.
- **Make changes easy to delete.** Prefer loosely coupled, well-bounded changes that can be removed cleanly.
- **Use boring technology.** Prefer familiar, proven tools and existing infrastructure over clever or novel approaches.
- **Design for testing.** Favor determinism, and factor logic so it can be tested in isolation. Thinking through how you would test it often improves the design even if you do not write the tests yet.
- **Correct before fast.** Prioritize correctness over performance unless performance is a stated requirement.
- **Change things properly.** Make clean changes at the appropriate design boundary; avoid expedient patches that create future debt.

An invented illustration of the first principle, as a code comment:

```
# Every reminder goes through the job queue, even when the recipient
# is on the same server. A direct shortcut for local recipients would
# create two delivery paths, and bugs would only appear depending on
# where a request happened to land. One path is easier to test.
```

An invented illustration of what to avoid under the second principle:

```python
try:
    total = calculate_order_total(order)
except (ValueError, TypeError, KeyError, AttributeError):
    total = 0.0  # hides real bugs as a believable but wrong number
```

If `calculate_order_total` raises `AttributeError`, that is a bug. It should fail loudly, not quietly report a zero total.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

A compact comparison table often helps. An invented example for Fernwood Garden Club, which wants members to stop missing volunteer shifts:

| Option | Fits criteria? | Main cost | Main risk |
|---|---|---|---|
| Do nothing | Yes, but problem persists | None | Shifts keep going unfilled |
| Shared calendar plus weekly reminder email | Yes | An hour of setup | Reminders get ignored |
| Custom sign-up program with text alerts | Partly; adds a new dependency | Days of work, ongoing upkeep | Hard to remove once members rely on it |

Recommendation: the shared calendar with reminders, because it solves the main problem with existing tools and is easy to undo. Revisit a custom program only if missed shifts continue.

Keep the proposal direct. Expect the decision-maker to ask questions or iterate before choosing; they may pick a different option.

By default, give the proposal directly in your reply. Only move it into a separate shared document when the user asks for one, and then follow their usual documentation practice. Do not park proposals in loose local files the reader has to go find and open. If you do create a document, give it a clear, date-prefixed title, using one unambiguous date format consistently (spelling out the month, as in `9 Oct 2026: Solve - topic`, avoids day/month confusion).

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration and rollback strategy, test strategy, deployment steps, and follow-up ownership. Put the plan somewhere reviewers can easily read, comment on, and edit.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, security, and failure behavior.

Do not claim success based only on implementation. State what was tested, the results, and what remains unverified. Commit, publish, or deploy changes according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.

## Common failure modes

- Building exactly what was asked when the request does not solve the real problem.
- Skipping criteria, so the first plausible idea wins.
- Offering only technical options, or only variations of one design.
- Leaving out "do nothing" when the priority is weak.
- Presenting several options without a recommendation.
- Slipping a hard-to-reverse commitment into implementation without an explicit decision.
- Writing long proposals that bury the recommendation.
- Sending the reader off to a separate file or document they did not ask for instead of answering in the reply.
- Reporting "done" without saying what was verified.

## Optional extras

- **Shared documents.** If the user asks for the proposal as a shared document, create it in their chosen documentation system with the date-prefixed title, following their usual conventions for location and sharing, and end your reply with a link. For larger implementation plans, editable shared documents are usually easier for reviewers than plans kept inside an assistant's private planning mode. Plans for pure code changes tied to a single branch can stay with the code if the user prefers.
- **Repository conventions.** If the user's practice is to commit and push after completing work, follow it, including any commit message prefixes (for example, feature, fix, or maintenance tags). Otherwise ask before publishing.
- **Wide idea generation.** For problems that need many candidates, run a separate brainstorm aiming for a large list (for example, ten or more ideas, adjustable) before narrowing to the few worth comparing.
- **Decision records.** For hard-to-reverse choices, keep a short record of the options considered, the choice, the rationale, and what would cause you to revisit it.

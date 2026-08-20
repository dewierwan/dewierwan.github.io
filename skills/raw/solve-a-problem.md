---
name: solve-a-problem
description: Take a messy problem from diagnosis through research, options, recommendation, and implementation.
---

# Solve a problem

Use this for a non-trivial build, process, automation, or operational problem
whose solution is not yet obvious.

## 1. Understand the problem

Start from the user's underlying problem rather than their first proposed
solution. Define who is affected, what they are trying to achieve, how often the
problem occurs, and what makes the current situation costly.

## 2. Decide whether to solve it now

Compare the problem with other work competing for attention. Consider a manual
workaround or doing nothing. If the issue is rare and cheap, say so.

## 3. Research the current system

Read the relevant instructions, code, examples, history, and existing patterns.
Look for prior attempts and constraints. Do not ask the user for facts available
in the system.

## 4. Define success

Write a short set of testable criteria. Include the result, safety constraints,
maintenance limit, and how the solution will be verified.

## 5. Generate varied approaches

Consider:

- A process or instruction change.
- A small technical change.
- A larger integrated solution.
- An existing service or platform feature.
- Doing nothing.

Evaluate each honestly. Prefer a simple, conventional solution with one clear
path over a flexible system full of branches and settings.

## 6. Recommend and implement

Recommend one approach with its tradeoffs. Once approved, make an implementation
plan, build it, and verify it against the success criteria. Fail loudly when a
required condition is missing. Do not silently return a weaker result.

## 7. Hand off

Report the outcome, tests run, remaining risks, and any action the user must
take. Keep temporary implementation detail out of the handoff.

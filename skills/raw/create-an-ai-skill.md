---
name: create-an-ai-skill
description: Turn a repeated workflow into a focused skill, test when it triggers, and improve it using real examples.
---

# Create an AI skill

Use this when a repeated task deserves reusable instructions.

## 1. Define the job

Collect several examples of requests that should trigger the skill and nearby
requests that should not. State the user's desired result, inputs, available
tools, safety limits, and definition of completion.

## 2. Choose the scope

Make one skill responsible for one coherent job. Split workflows when they have
different audiences, permissions, sources of truth, or completion conditions.
Avoid a giant instruction file that tries to govern unrelated work.

## 3. Write the description

Describe what the skill does and the language users are likely to use when they
need it. Include important exclusions that prevent false triggering. Do not use
the description as a full summary of the workflow.

## 4. Write the workflow

Use clear sections, concrete actions, decision points, and failure behavior.
Name required sources and tools by capability. State when to ask the user, when
to proceed, and which actions need approval. Prefer a short reliable path over
many configurable branches.

## 5. Test it

Create a small evaluation set with positive, negative, easy, ambiguous, and
failure cases. Check:

- Did the skill trigger at the right time?
- Did it use the right evidence?
- Did it follow permissions?
- Did it produce a verifiable result?
- Did it avoid unnecessary questions and work?

## 6. Improve from evidence

Revise the smallest instruction responsible for each failure. Re-run the full
evaluation set to catch regressions. Add real lessons after use, then consolidate
old rules so the skill remains readable.

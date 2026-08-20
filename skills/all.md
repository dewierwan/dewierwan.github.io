# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly.


---
name: brainstorm
description: Generate genuinely different options, compare them honestly, and choose the strongest ones.
---

# Brainstorm options

Use this skill when the user wants possible approaches, directions, names, or
solutions and does not yet know which one to choose.

## 1. Frame the problem

State the decision in one sentence. Clarify the desired result, the people
affected, the main limits, and what has already been tried. Ask only for facts
that would change the options.

## 2. Generate distinct options

Create options from different underlying approaches. Do not produce small
variations of the same idea. Include:

- A simple or low-effort approach.
- A bold approach.
- An approach that changes the process rather than adding more work.
- A combination only when its parts genuinely fit together.
- Doing nothing when it is a serious option.

For a complex problem, generate widely before narrowing. Remove duplicates and
weak filler before showing the user.

## 3. Evaluate them

Choose a small set of criteria that match the real decision. Compare each option
on likely impact, effort, risk, reversibility, and speed. Add any domain-specific
criterion that matters more.

Name the strongest advantage and weakness of every serious option. Do not make
the preferred option look good by describing the alternatives badly.

## 4. Recommend

Recommend one option or a short ranked list. Explain which tradeoff drives the
recommendation. State the assumption most likely to change the ranking.

End by asking whether the user wants to choose, combine, or develop any option.


---
name: pressure-test
description: Find the weak points in an idea before committing to it. Test assumptions, objections, and likely failure modes.
---

# Pressure-test an idea

Use this when the user is leaning toward an important idea and wants a serious
attempt to find where it could fail.

## 1. State the idea fairly

Summarize the idea, its intended result, and why a reasonable person would
support it. Ask the user to correct the summary before attacking it.

## 2. Find the load-bearing assumptions

List the few assumptions that must be true for the idea to work. Separate facts,
estimates, and beliefs. For each assumption, ask what evidence supports it and
what evidence would disprove it.

## 3. Ask forcing questions

Ask one question at a time. Prefer questions that force a choice or reveal a
tradeoff:

- What must go unusually well?
- Who has an incentive to resist this?
- What important cost is missing?
- What happens at ten times the expected scale?
- Which part cannot be reversed?
- What would a thoughtful critic say is naive?

Adapt later questions to the user's answers rather than reading a fixed list.

## 4. Run a pre-mortem

Imagine the idea failed after a realistic period. Give several specific causes,
including one caused by execution, one caused by the environment, and one
caused by a wrong premise. Identify the earliest warning sign for each.

## 5. Judge the idea

Give a clear result:

- **Proceed:** the main risks are understood and manageable.
- **Test first:** one or more assumptions need cheap evidence.
- **Stop or redesign:** a core weakness makes the current version unsound.

End with the smallest action that would reduce the most uncertainty.


---
name: make-a-decision
description: Match the amount of analysis to the stakes, compare the real options, and record what would change the decision.
---

# Make a decision

Help the user decide without turning every choice into a research project.

## 1. Define the decision

Write the decision as a choice between concrete options. Clarify who decides,
the deadline, the desired result, and what happens if nobody acts.

## 2. Match effort to reversibility

- For a cheap, reversible choice, set a short deadline and choose quickly.
- For a costly but reversible choice, compare the main evidence and run a test.
- For a hard-to-reverse choice, examine assumptions, dissent, and failure modes.

Do not use more analysis than the decision deserves.

## 3. Compare the options

Choose criteria before scoring options. Separate requirements from preferences.
Use numbers only when they clarify rather than hide judgment.

For each serious option, record:

- What becomes possible.
- What it costs or prevents.
- The strongest evidence for it.
- The strongest objection.
- How easy it is to reverse.

## 4. Make the call

Recommend one option and explain the decisive reason. State any remaining
uncertainty plainly. If evidence is missing, propose the cheapest test that can
change the decision rather than gathering information without a stopping rule.

## 5. Record and review

For a meaningful decision, record the choice, alternatives, rationale,
prediction, worries, and what would change the user's mind. Set a review point
only when later evidence could lead to a useful correction.


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


---
name: shape-and-draft
description: Develop consequential documents by shaping the underlying decisions before drafting. This workflow uses evidence, successive answer-dependent interview rounds, an alignment ledger, a readiness gate, and a final audit.
---

# Shape and draft a document

Develop an important document by first shaping the thinking behind it. Earn the draft: determine what the document must achieve, gather relevant evidence, and resolve material uncertainty with the user before writing.

Use this workflow for consequential strategies, narratives, operating agreements, briefs, proposals, scorecards, and decision memos when the desired artifact or underlying thinking is not fully settled. Do not use it for quick edits or documents whose content is already specified.

## Input and request classification

The request may name a proposed document, desired outcome, audience, source material, or some combination. Treat the proposed document type as a hypothesis until its purpose is clear.

Treat the work as a **full shaping request** when the document is strategically consequential and its argument, boundaries, commitments, or operating model remain materially unsettled, or when the user asks for deep thinking, extensive questions, multiple rounds, or near-complete alignment.

A substantive round resolves a distinct layer of choices and uses the user's answers to determine the next layer. A restatement or request for general approval does not count as a substantive round.

## 1. Work backwards from the outcome

Start with the change the document needs to produce. Determine:

- Who will read it?
- What should they understand, decide, or do afterward?
- What is unclear, contested, or currently going wrong?
- Does the document mainly need to explain, persuade, decide, coordinate, or govern?

Do not accept “write a narrative” or “make a strategy page” as the goal. Identify the job the document must do.

## 2. Choose the artifact

Choose the form that best serves the goal:

- **Narrative:** Builds shared understanding of why something matters and the bet being made.
- **Strategy:** Connects a diagnosis to choices, priorities, outcomes, and exclusions.
- **Operating agreement:** Defines ownership, interfaces, decision rights, handoffs, and cadence.
- **Decision memo:** Records a choice, alternatives, rationale, risks, and review point.
- **Scorecard:** Defines a role or team’s mission, outcomes, and capabilities.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the tradeoff and recommend one. If the choice is load-bearing, ask the user to confirm it before going deeper.

## 3. Gather evidence

Read supplied sources first. Apply any stated source-selection, source-of-truth, and evidence-linking rules. Scale research to the stakes. For a high-stakes strategy document, examine available material most likely to contain prior decisions, current definitions, relevant evidence, dissent, and ownership context.

Follow these rules:

- Respect any stated source-of-truth hierarchy.
- Treat discussion notes and generated summaries as weaker than canonical decisions.
- Resolve contradictions where possible and surface the remainder.
- Do not ask the user for facts that available sources can answer.
- Do not alter supplied source material unless the user explicitly asks.

Maintain a strict boundary between evidence and alignment:

- Sources can establish what happened, what people said, and what an authoritative record currently states.
- Sources do not establish what the user now believes, wants to promise, or is willing to exclude unless they contain an explicit, current decision from the user.
- Treat a synthesis, repeated theme, or plausible implication as **inferred**, not settled.
- Ask the user to confirm an inferred position if it would become a central claim, commitment, boundary, or recommendation.

Before interviewing, provide a short situation brief covering:

- What sources establish.
- What the user has already confirmed.
- What is inferred but unconfirmed.
- The central tension or missing logic.
- The recommended artifact.
- Important uncertainties only the user can resolve.

## 4. Interview in successive rounds

For a full shaping request, complete at least two substantive, answer-dependent interview rounds before drafting. Count relevant rounds already completed in the current conversation; do not repeat them. Do not draft immediately after the first answer round, even if one apparent core tension is resolved. The second round should test implications, boundaries, counterarguments, or execution details revealed by the first.

Ask 4 to 8 focused questions per round. If fewer than four material questions genuinely remain, ask all of them and state that this is a narrow final check. Do not inflate a round with ritual questions.

One numbered question should normally contain one decision. Do not bundle independent choices, such as ownership, coordination, handoffs, and success measures, into one yes/no question. Broad answers to bundled questions create false alignment.

Format questions for fast, unambiguous replies:

1. Number every question: `1.`, `2.`, `3.`.
2. Label bounded options with lowercase letters: `a.`, `b.`, `c.`.
3. Put the recommended option at `a.` unless prior context makes another ordering clearer.
4. Render the entire question block as a compact, single-spaced list, with each question and option on consecutive lines and no blank lines between them.
5. Do not use hard-break characters or HTML line-break tags.

Example:

1. Which direction should we take?
   a. Recommended direction.
   b. More cautious direction.
   c. More ambitious direction.
2. Who should own it?
   a. The program lead.
   b. The functional lead.

Each round should:

1. Start with the updated model and explain what changed because of prior answers.
2. Focus on one layer of uncertainty.
3. Offer two or three concrete options when the choice can be bounded.
4. Put the recommended option first and explain its tradeoff briefly.
5. Leave room for the user to reject the framing or provide a different answer.
6. Notice contradictions and ask the smallest question needed to resolve them.
7. Separate what sources suggest from what the user must decide.
8. Include at least one pressure-test of the emerging position for persuasive or strategically consequential documents.

A typical progression is:

1. **Purpose:** Audience, desired effect, artifact type.
2. **Strategy:** Diagnosis, central bet, priority, scope, exclusions.
3. **Operating model:** Owners, interfaces, handoffs, decision rights.
4. **Definitions:** Thresholds, edge cases, success measures, evidence standards.
5. **Expression:** Tone, length, destination, and deliberate open questions.

After every answer round, do all four steps before deciding whether to draft:

1. Classify each answer as confirming, rejecting, softening, qualifying, or deferring the proposed position.
2. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing normally creates another question.
3. Update and show a concise synthesis of the alignment ledger.
4. Generate the next round from remaining material uncertainties and the consequences of the answers.

Continue while an uncertainty could materially change the draft. Stop only after at least two substantive rounds and the readiness gate. If the user explicitly asks to skip further questions and draft now, briefly explain the material consequence and follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record throughout the conversation:

- **Confirmed:** Choices the user explicitly made, including relevant earlier decisions.
- **Source facts:** Claims established by current, authoritative evidence but not selected by the user.
- **Inferred:** Current interpretation, clearly distinguished from a decision.
- **Open:** Questions that could materially change the document.
- **Corrected:** Assumptions or source claims the user rejected.

After every answer round, update this model before asking more questions. Never reintroduce a corrected assumption. If two confirmed statements appear inconsistent, surface and resolve the conflict rather than smoothing it over. Never promote an inference to confirmed merely because several sources support it.

For a full shaping request, show the user a concise updated model before each later round so they can catch mistaken assumptions. Every major claim planned for the draft must be confirmed, a source fact, or deliberately presented as a proposal or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document’s substance. Before drafting, explicitly rerun the gate and give a concise pre-draft synthesis of:

- Intended job.
- Audience.
- Central position.
- Important boundaries.
- Deliberate open questions.

For each major claim in the anticipated outline, ask: **Did the user confirm this, does an authoritative source establish it as fact, or am I merely inferring it?** If it is a material inference, ask another question instead of drafting.

Check that every relevant category is confirmed, established by evidence, deliberately left open, or genuinely not applicable:

- Goal and audience.
- Artifact type.
- Central argument or bet.
- Scope and exclusions.
- Definitions and thresholds.
- Ownership and decision rights.
- Interfaces and handoffs.
- Success measures and evidence standard.
- Tone, length, and destination.

For persuasive documents, complete a skeptical-reader pass:

- What is the strongest objection from the actual audience?
- Which premise, commitment, evidence, or safeguard would they dispute?
- Has the user confirmed the response the draft will give?

Resolving one central tension is insufficient if the draft still depends on unconfirmed positions about theory of change, scope, relationship model, commitments, evidence, or exclusions.

“Near-complete alignment” does not mean a literal probability. It means remaining uncertainty is low impact, or the document explicitly represents it as unresolved.

If the user asks for a draft before the gate is met, name one or two consequences of the uncertainty and then follow the instruction.

## 7. Draft

Follow the user’s stated voice, style preferences, and delivery requirements. Write the smallest document that can do the job. Prefer clear claims, concrete decisions, and explicit ownership over polished abstractions. Distinguish current decisions from proposals and future review points.

Honor the requested destination and format using the user’s chosen system. If the user asks for text in the conversation, provide text only and do not alter source material. If the user asks for a document to be created or edited, produce the requested deliverable in the chosen system and verify that it contains the intended content.

## 8. Audit before delivery

Compare the draft with the alignment ledger and source hierarchy:

- Does it solve the agreed problem in the agreed form?
- Does every material choice reflect the user’s answers?
- Are corrected assumptions gone?
- Are responsibilities, boundaries, and handoffs unambiguous?
- Are uncertain claims marked as such?
- Are factual claims and citations supported by sources?
- Is anything presented as settled that was only inferred?
- Does the draft match the requested voice rather than sounding like an external consultant?

Fix every mismatch before delivering. Put the deliverable last, with no trailing summary or offer that would interfere with copying it.

## Failure modes to avoid

- Drafting early because producing text feels useful.
- Treating the proposed artifact as fixed.
- Asking questions before researching answerable facts.
- Mistaking extensive research for alignment with the user.
- Treating a plausible synthesis as a decision.
- Sending a generic questionnaire disconnected from evidence.
- Failing to update the model after each answer.
- Drafting after one round because a single core tension appears resolved.
- Bundling several independent decisions into one question.
- Skipping a consequence round after the user softens or qualifies a claim.
- Repeating a question the user already answered.
- Hiding contradictions behind vague language.
- Continuing interviews after only low-impact uncertainties remain.
- Producing an inspiring narrative that leaves ownership or decisions unclear.


---
name: gather-context
description: Search the sources that are likely to matter and turn the findings into one concise, well-sourced brief.
---

# Gather context

Use this when the user needs to understand a person, organization, project,
topic, or decision before acting.

## 1. Choose the effort level

- **Quick:** Check a few obvious sources and answer briefly.
- **Standard:** Search several relevant sources and produce a compact brief.
- **Deep:** Search broadly, verify important claims, and resolve contradictions.

Match the effort to the stakes. Do not search every available system by habit.

## 2. Choose relevant sources

Select sources based on the subject. Possible capabilities include email,
messages, documents, meeting notes, calendar, transcripts, databases, code,
and the public web. Named sources are required, but add another source when it
clearly holds decision-relevant evidence.

Search with more than one useful query for a deep review. If a recent meeting
appears in the results, read its notes or transcript.

## 3. Judge evidence

Prefer primary and current sources. Treat summaries and discussion as weaker
than canonical decisions. Resolve conflicts when possible and state what remains
uncertain. Never invent a link or imply that an unavailable source was checked.

## 4. Synthesize by theme

Lead with what matters for the user's intended action. Organize the brief around
the subject, not around the tools searched. A useful structure is:

- Short summary.
- What is known.
- Relevant history or relationship.
- Current decisions and ownership.
- Open questions and missing evidence.
- Direct source links.

Every sourced claim should let the user reach its supporting evidence.


---
name: learning-tutor
description: Learn a topic through short explanations, active recall, and questions that adjust to your understanding.
---

# Learn with a tutor

Teach through conversation rather than delivering a long lecture.

## 1. Set the target

Ask what the learner wants to understand or be able to do. Find their current
level, relevant background, and available time. Agree on a small learning goal.

## 2. Build a map

Break the topic into a few connected ideas. Start with the concept that makes
the others easier. Explain where the current lesson fits in the map.

## 3. Teach in short cycles

For each idea:

1. Explain it in plain language.
2. Give one concrete example.
3. Ask one question that requires recall or application.
4. Wait for the answer.
5. Correct the learner directly and explain the gap.

Do not reveal the answer before the learner attempts the question. Ask one
question per message unless the learner requests a worksheet or test.

## 4. Adjust

If the learner is confused, change the representation: use an analogy, a
diagram described in words, a smaller example, or a comparison. If they answer
easily, increase difficulty or ask them to transfer the idea to a new case.

## 5. Consolidate

At useful intervals, ask the learner to explain the idea in their own words.
End with a short recap, one retrieval question for later, and the next concept
that follows naturally.


---
name: write-in-my-voice
description: Use a personal style guide to draft messages that sound like the user instead of generic AI writing.
---

# Write in my voice

Use this when drafting a message, post, brief, or document on the user's behalf.

## 1. Load the style evidence

Read the user's current style guide in full. If available, compare several real
examples written by the user with earlier AI drafts. Recent user edits are
stronger evidence than general writing advice.

Extract rules about:

- Openings and closings.
- Sentence length and paragraph rhythm.
- Formality and warmth.
- Words and punctuation the user avoids.
- How direct requests, disagreement, praise, and uncertainty sound.
- Facts or standard wording that may be reused safely.

## 2. Separate voice from content

Do not invent beliefs, commitments, facts, or emotional reactions because they
would sound plausible in the user's voice. Confirm important positions and
verify facts first.

## 3. Draft for the situation

Match the audience, relationship, channel, and stakes. Use the smallest amount
of context needed. Prefer concrete nouns and short sentences. Remove throat
clearing, process explanations, hollow praise, repeated appreciation, and
generic closing lines.

## 4. Audit against real examples

Check the draft line by line against the style guide. Ask:

- Would the user choose these words?
- Is any sentence longer or more polished than their normal writing?
- Did the draft add an opinion or promise they did not state?
- Can anything be cut without losing the action or meaning?

Put copy-ready text last with no commentary after it.


---
name: professional-social-post
description: Turn notes or source material into a clear social post with a strong opening and a specific point.
---

# Write a professional social post

Use this to draft, revise, or critique a post based on real source material.

## 1. Find the point

State the one idea the reader should remember. Identify the intended reader and
why the idea matters to them now. If the source contains several ideas, choose
one instead of summarizing everything.

## 2. Choose the shape

Useful shapes include:

- A surprising observation followed by its explanation.
- A concrete story followed by the lesson.
- A common belief corrected with evidence.
- A useful framework applied to a real problem.
- A result, how it happened, and what others can learn.

## 3. Draft the opening

Write several openings that create honest curiosity. Prefer a specific claim or
scene. Avoid vague drama, exaggerated stakes, and generic announcements.

## 4. Build the post

Use short paragraphs. Move from opening to evidence to implication. Include
only details that support the point. Preserve uncertainty and avoid claiming
causation when the evidence shows only correlation.

End with a useful conclusion, question, or clear action when one follows
naturally. Do not add a forced invitation to comment.

## 5. Remove AI habits

Cut inflated adjectives, repetitive sentence openings, unnecessary contrasts,
abstract slogans, long setup, and claims that could apply to any organization.
Read the post aloud and shorten lines that sound performed rather than spoken.


---
name: case-study-post
description: Turn a person's real change into a short, evidence-based case study without exaggerating their story.
---

# Write a case study post

Use this when source material describes a person's starting point, an
intervention or experience, and what changed afterward.

## 1. Build the evidence

Read the person's own words, timeline, work, and verified outcomes. Separate
facts from interpretation. Check names, roles, dates, figures, and quotations
against primary sources. Mark anything that needs the person's approval.

## 2. Find the story

Extract three beats:

1. **Before:** the specific problem, uncertainty, or constraint.
2. **Change:** what the person did and what helped.
3. **After:** the concrete result and remaining limits.

Do not claim that one program, product, or mentor caused the full outcome unless
the evidence supports it.

## 3. Choose an honest opening

Lead with the most specific and human part of the change. Avoid presenting the
person as a symbol, flattening their motivation, or using private hardship as a
hook without consent.

## 4. Draft concisely

Write short paragraphs with a clear sequence. Use exact evidence and at most one
quotation when it adds a distinct truth. Explain the mechanism, not only the
result. End with the wider lesson or a relevant action.

## 5. Approval check

Before publication, flag sensitive facts, money, health, employment changes,
direct quotations, and any claim about causation for the subject to approve.


---
name: plan-your-day
description: Choose one most important outcome, protect time for it, and make a realistic plan around existing commitments.
---

# Plan your day

Use this when the user wants to choose priorities, schedule work, or recover a
day that has become reactive.

## 1. Read the real day

Check the calendar, current tasks, deadlines, unfinished commitments, energy,
and any personal constraint the user chooses to share. Use the user's local
date and time. Do not propose work inside existing commitments.

## 2. Choose one most important outcome

Ask what result would make the day count. Turn it into a binary finish line,
such as sending a draft or making a decision. Avoid labels such as “work on” or
“make progress.”

Test the choice:

- Is it important rather than merely urgent?
- Can the user influence the result today?
- Does it fit the available focused time?
- Is another task more likely to be productive-looking avoidance?

## 3. Protect a focused block

Find the best uninterrupted window and match the task to the user's likely
energy. Break long work into realistic chunks with short breaks. Include setup
and a clear first action so the block begins without another decision.

## 4. Fit the rest around it

Choose a small number of secondary tasks. Batch shallow work. Remove or defer
anything that makes the plan implausible. Leave space for meals, movement,
travel, recovery, and unexpected work.

## 5. Pre-mortem

Ask what displacement work is most likely to steal the focused block. Name one
specific counter, such as closing messages, preparing the source document, or
starting before a meeting-heavy period.

## 6. Record the plan

Write the outcome, focused block, secondary tasks, and main risk into the user's
chosen planning system. Confirm that the plan fits the calendar before creating
or moving events.


---
name: review-your-day
description: Run a short end-of-day reflection on what happened, what mattered, and what should change tomorrow.
---

# Review your day

Use this at the end of the day before planning tomorrow.

## 1. Reconstruct the day

Read the plan, calendar, completed work, and any notes the user has chosen to
record. Ask what actually happened rather than assuming that calendar blocks
were completed.

## 2. Reflect briefly

Ask one question at a time:

1. What shipped compared with the plan?
2. What was the main win?
3. What drained energy or created friction?
4. What needs to be carried, delegated, or dropped?

If the most important outcome did not ship, ask what felt productive but did
not move it. Name the pattern without moralizing.

## 3. Extract learning

Distinguish a one-off disruption from a repeated problem. Look for a change to
the environment, task definition, timing, or commitment level that could make
tomorrow easier.

## 4. Record accurately

Write a concise journal entry in the user's chosen system. Preserve the user's
words and do not invent an emotional interpretation. If the system uses a
rating, ask the user rather than inferring it.

## 5. Close

End with the one fact tomorrow's plan should account for. Do not turn the review
into a full planning session unless the user asks to continue.


---
name: plan-your-week
description: Review the previous week, choose a few outcomes, cut lower-value work, and protect time for what matters.
---

# Plan your week

Use this to review the last week and commit to the next one.

## 1. Gather the week

Read the previous plan, current goals, calendar, overdue tasks, important
messages, and any personal commitments the user includes. Check that sources are
current before relying on them.

## 2. Review the previous week

Ask what shipped, what rolled over, and what the week taught the user about
capacity. Treat unfinished goals separately:

- Roll over when the goal still matters and has a credible path.
- Demote when it matters but does not deserve a weekly commitment.
- Drop when keeping it active creates noise without action.

## 3. Choose a few outcomes

Select one to three results that can be judged at the end of the week. If the
calendar is dominated by meetings, logistics, or care for other people, plan a
week that reflects that reality rather than pretending it is a writing retreat.

## 4. Cut work

Identify meetings, tasks, and projects that do not serve the chosen outcomes.
For long-deferred tasks, consider moving them out of the active backlog rather
than assigning another false deadline.

## 5. Pre-mortem

Ask what will most likely displace each outcome. Add one prevention or recovery
step. State what the user is deliberately deprioritizing.

## 6. Break down and schedule

Turn each outcome into clear tasks. Propose focused blocks around fixed
commitments, then recheck the live calendar before writing events. Do not create
tasks whose shape depends on an unresolved decision.

## 7. Record the commitment

Write the outcomes, rollover decisions, protected blocks, risks, and cuts into
the user's planning system. Keep the final plan short enough to guide the week.


---
name: review-and-plan-a-month
description: Close one month honestly, choose a theme for the next, and turn it into a small set of concrete commitments.
---

# Review and plan a month

Use this at the boundary between months.

## 1. Gather evidence

Read the previous monthly plan, weekly plans, calendar, completed projects,
important metrics, and personal notes the user chooses to include. Separate what
happened from what was intended.

## 2. Review the month ending

Ask:

- What changed because of this month's work?
- Which commitment mattered most?
- What repeatedly slipped?
- What used time without producing enough value?
- What should continue, stop, or be redesigned?

Use evidence where possible and preserve the user's interpretation where the
evidence cannot answer.

## 3. Choose a theme

Name one useful theme for the next month. It should guide tradeoffs, not act as
a slogan. Explain what the theme makes more important and what it makes less
important.

## 4. Set commitments

Choose a small set of outcomes that fit known capacity and fixed commitments.
Define a finish line and evidence for each. Include personal or health goals
only when the user wants them in scope.

## 5. Pre-mortem and record

Identify the main reason the plan could fail and one countermeasure. Write the
review and new plan into the user's chosen system. Carry forward only work the
user explicitly recommits to.


---
name: get-unstuck
description: Work out why you are stuck, then use a short intervention suited to tiredness, dread, confusion, or distraction.
---

# Get unstuck

Use this when the user says they are tired, avoiding work, distracted, dreading
a task, or unable to begin.

## 1. Diagnose before coaching

Ask one short question at a time. Distinguish among:

- **Physical:** tired, hungry, uncomfortable, or overstimulated.
- **Dread:** the task carries conflict, judgment, or emotional cost.
- **Unclear:** the next action or standard is vague.
- **Distracted:** the environment keeps offering easier rewards.

More than one can be true. Do not treat an exhausted person as if they only need
discipline.

## 2. Choose a short intervention

Match the response to the diagnosis:

- Physical: food, water, movement, rest, or a smaller task.
- Dread: name the feared outcome and reduce the social or emotional exposure.
- Unclear: define the next visible action and a deliberately rough first pass.
- Distracted: change the environment and remove the competing cue.

Keep the intervention short. The aim is to begin useful motion, not hold a long
coaching conversation.

## 3. Start together

Ask the user to take one action that lasts only a few minutes. When useful,
write the opening line, checklist, or tiny plan with them. Confirm what “started”
means.

## 4. Learn from the result

After the attempt, ask what helped. Record patterns only with the user's
permission. Adapt future interventions to observed results rather than assuming
one motivational style always works.


---
name: wind-down-for-sleep
description: Guide a short evening routine that closes open loops, prepares the environment, and makes sleep easier.
---

# Wind down for sleep

Use this when the user wants help ending the day or cannot settle for sleep.

## 1. Check the situation

Ask whether the day has been reviewed and tomorrow has been planned. Check the
next morning's first fixed commitment if the user has calendar access. Keep the
routine shorter when it is already late.

## 2. Close the environment

Guide a brief checklist chosen by the user, such as:

- Put work materials away.
- Set the phone or distracting devices outside reach.
- Prepare clothes, water, medication, or morning essentials.
- Adjust light, temperature, and noise.

Ask for confirmation after each small group rather than delivering a long list.

## 3. Offload tomorrow

Capture any remaining thought that is keeping the mind active. Write a short
morning note with the first action and anything that must not be forgotten. Do
not reopen planning unless a genuine conflict appears.

## 4. Settle

Offer one short, low-stimulation practice the user already accepts, such as slow
breathing, body awareness, or quiet reading outside bed. Avoid turning sleep
into a performance test.

## 5. If sleep does not come

If the user remains awake and frustrated, suggest leaving the bed for a calm,
dim activity until sleepiness returns. Keep clocks and stimulating content out
of view. For persistent sleep problems, recommend appropriate professional
support rather than expanding the routine indefinitely.


---
name: prepare-for-a-meeting
description: Gather the relevant history, clarify the desired outcome, and produce a focused agenda and preparation brief.
---

# Prepare for a meeting

Use this before a consequential meeting or when the user asks for an agenda.

## 1. Read the meeting

Check the invitation, attendees, timing, stated purpose, and linked materials.
Read any supplied proposal, document, or deck in full before drafting an agenda.

## 2. Gather context

Search the sources most likely to contain the relationship history, prior
decisions, promises, open questions, and recent changes. A recent transcript or
meeting note often matters more than older summaries.

Distinguish facts, other people's views, and the user's current position. Do not
infer what the user wants to promise.

## 3. Ask focused questions

Before drafting, summarize what the evidence establishes and ask a small number
of questions about:

- The desired result.
- The user's current stance.
- Sensitive topics or boundaries.
- Decisions that can and cannot be made in the meeting.

## 4. Prepare the brief

Include:

- The meeting's job.
- Essential context.
- The user's desired outcome.
- A short agenda ordered by importance.
- Questions to ask.
- Likely objections or difficult moments.
- Decisions, owners, and follow-up to capture.

Keep the agenda realistic for the available time. Put the most important topic
before status updates and background.


---
name: capture-meeting-actions
description: Review meeting notes, identify genuine commitments, create clear tasks, and ask about uncertain cases.
---

# Capture meeting actions

Use this to turn meeting notes or transcripts into reliable follow-up.

## 1. Read the complete record

Read all available meeting notes and the relevant transcript when attribution or
wording matters. Identify who made each commitment. Do not assign every idea or
suggestion as a task.

## 2. Extract candidate actions

An action should have an owner and a concrete result. Capture:

- Explicit promises.
- Requests accepted by someone.
- Decisions that require implementation.
- Follow-up needed to unblock another person.

Exclude observations, possibilities, repeated work already tracked, and actions
owned by someone else unless the user needs to monitor them.

## 3. Clarify the task

For each action, write a short verb-led title, a finish line, useful context,
source link, and due date only when the meeting established one. Preserve any
important wording from the commitment without copying private discussion into a
broadly visible task system.

## 4. Handle uncertainty

Create high-confidence tasks without interruption when authorized. Batch
uncertain cases at the end and ask the smallest question needed to resolve
ownership, scope, or timing.

## 5. Verify

Check for duplicates and confirm that every created task points back to the
meeting record. Report created actions and unresolved questions separately.


---
name: turn-a-message-into-a-task
description: Read the full conversation, work out the real action, do useful preparation, and create a clear task only when needed.
---

# Turn a message into a task

Use this when a conversation contains a request or follow-up that may need a
task record.

## 1. Read the whole conversation

Open the parent message and all replies. Identify the people involved, the
actual request, promises already made, deadlines, links, and whether someone has
already completed the work.

## 2. Work out the real action

Rewrite the request as an outcome. Separate the user's action from work owned by
other people. If the message can be answered or resolved immediately, do that
instead of creating a task for its own sake.

## 3. Gather enough context

Check relevant documents, prior conversations, meeting notes, records, or public
sources when they can answer factual questions. Match research effort to the
stakes. Do not delay a simple task with an exhaustive search.

## 4. Do useful preparation

When authorized, draft the reply, assemble the figures, outline the document,
or prepare the decision before creating the record. Keep actions that affect
other people in draft form until the user approves them.

## 5. Decide whether a record helps

Create a task when work remains, it may be forgotten, or another commitment
depends on it. Skip the record when the action is complete, trivial, duplicated,
or better owned elsewhere.

## 6. Create a useful task

Use a clear title, binary finish line, relevant context, source link, owner, and
real deadline. Avoid copying a whole conversation into the notes. Verify the
record after writing it.


---
name: design-a-work-sample
description: Create a short paid exercise that tests the real work of a role and distinguishes strong from weak performance.
---

# Design a work sample

Use this to create or improve a time-limited hiring exercise.

## 1. Understand the role

Read the role description, outcome expectations, team context, and examples of
strong real work. Identify the few abilities that predict success and can be
observed in a short exercise.

## 2. Write an assessment memo

Before drafting the exercise, state:

- What is being tested and why it matters.
- What evidence strong performance would produce.
- What should not affect the score.
- Which abilities cannot be tested fairly in this format.

Confirm this logic with the hiring owner.

## 3. Generate exercise shapes

Consider several formats drawn from the actual role: diagnose a problem,
produce a small deliverable, improve flawed work, make a recommendation, or
handle a realistic simulation. Avoid unpaid production work and trivia that can
be looked up without judgment.

## 4. Draft clear instructions

Give the candidate the context, task, allowed tools, time limit, submission
format, and evaluation criteria. State how AI use should be handled. Remove
hidden expectations that insiders would know but candidates would not.

## 5. Validate the signal

Simulate at least two candidates:

- A strong candidate who has the target abilities.
- A polished but weak candidate who lacks a load-bearing ability.

Check whether the rubric separates them. Revise tasks that reward speed,
familiarity, or presentation more than the actual role.

## 6. Final checks

Ensure the work fits the stated time, respects accessibility needs, avoids
sensitive data, and can be scored consistently by different reviewers.


---
name: run-a-reference-call
description: Prepare and run a concise reference conversation that gathers specific evidence instead of vague praise.
---

# Run a reference call

Use this when checking a candidate's past work for a hiring decision.

## 1. Prepare from the decision

Read the role outcomes, interview evidence, remaining concerns, and the
candidate's relationship with the referee. Decide which uncertainty the call
must reduce. Do not ask a generic list when the hiring team already knows what
it needs to test.

## 2. Establish context

Confirm how the referee worked with the candidate, for how long, and how closely
they observed the relevant work. Weight evidence by direct observation rather
than title or confidence.

## 3. Ask for examples

Useful questions include:

- What result did the candidate personally own?
- What did strong performance look like in practice?
- Where did they need the most support?
- How did they respond to difficult feedback?
- Which environment helped or hurt their performance?
- What kind of role would you hesitate to place them in?
- Would you choose to work with them again, and in what capacity?

Follow vague praise with “What did that look like?” or “Can you give a specific
example?”

## 4. Test concerns fairly

Ask neutral questions about the hiring team's uncertainties without revealing
private interview judgments or inviting confirmation. Note contradictions and
seek concrete evidence.

## 5. Record signal

Separate observations, the referee's interpretation, and your inference. Record
confidence and any important limits on what the referee could know. Do not turn
one reference into a final verdict on its own.


---
name: use-a-browser-safely
description: Control websites carefully, inspect before acting, verify every change, and separate preparation from final submission.
---

# Use a browser safely

Use this for forms, account settings, rendered pages, or other work that needs
stateful interaction with a website.

## 1. Use a direct interface first

Prefer a documented application interface or purpose-built connector when it
can complete the task safely. Use browser control when the task genuinely
depends on the rendered page, an authenticated session, or visual state.

## 2. Protect the user's session

Use the correct account and browser profile. Open a new tab rather than taking
over unrelated work. Never expose stored credentials, copy private session data,
or weaken security settings to make automation easier.

## 3. Inspect before editing

Read the page structure, labels, current values, validation rules, and button
states. Confirm that the target account, record, and environment are correct.

## 4. Fill and verify incrementally

Use the input method suited to each control. After every meaningful change,
read the value back from the page. Watch for rich-text editors, character limits,
auto-formatting, hidden required fields, and controls that reset after navigation.

## 5. Separate preparation from commitment

Filling a form is usually reversible. Sending, purchasing, publishing, deleting,
or changing access may not be. Stop before the final action unless the user has
clearly authorized it. Show a concise summary of what will happen.

## 6. Verify the result

After submission, confirm the success state, resulting record, or changed
setting. A click without evidence is not completion. Close temporary tabs and
report anything that could not be verified.


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


---
name: test-every-screen-size
description: Check a user interface across narrow, wide, short, and tall screens using screenshots and numerical checks.
---

# Test every screen size

Use this after any visual or layout change and before declaring it complete.

## 1. Prepare realistic states

Run the real page in a test environment. Add representative long text, lists,
errors, loading states, and empty states. A clean screenshot with unrealistically
short content proves little.

## 2. Sweep widths and heights

Test at least these widths:

- 320
- 480
- 600
- 720
- 1024
- 1440
- 1920 for public landing pages

Use both a short and tall height where vertical layout matters. Include the
user's real working viewport when known.

## 3. Capture screenshots

Use a headless browser. Save a full-page image at each important size. Inspect
the top, right, bottom, and left edges of every changed component. Do not rely on
one mobile and one desktop screenshot.

## 4. Run numerical checks

For each width, check:

- No horizontal overflow.
- No elements overlap.
- Buttons and inputs remain visible and usable.
- Sticky or fixed elements do not cover content.
- Text lines remain within a readable measure.
- Focus states are visible.

Numbers catch subtle defects, while screenshots catch defects the numbers do
not describe. Use both.

## 5. Fix and repeat

If one size fails, correct the underlying layout and rerun the complete sweep.
A patch that fixes one viewport while breaking another is not complete.


---
name: run-a-recurring-community-event
description: Create a repeatable weekly event, prepare its materials, invite the right people, and verify every public detail.
---

# Run a recurring community event

Use this for a repeated social, learning, sports, or volunteer event.

## 1. Determine this occurrence

Calculate the correct date and sequence number from the calendar rather than
guessing. Read the previous event and note any approved changes to time, place,
capacity, host, or format.

## 2. Prepare the event materials

Create or update the title, description, image, location, accessibility details,
weather plan, equipment, and contact route. Keep stable information consistent
while making the date and any changed details unmistakable.

## 3. Create the event as a draft

Use the correct organizer account. Fill every field, then verify the public
preview before publishing. Check date, local time, time zone, map location,
host permissions, image crop, links, and capacity.

## 4. Choose invitees

Follow the user's standing invitation policy. Deduplicate previous attendees,
respect opt-outs and privacy, and avoid expanding the audience without
authorization. Add co-hosts only when their permission and account are clear.

## 5. Publish and verify

Publish only when authorized. Open the resulting public page and confirm every
important detail. Send invitations, then verify delivery or the resulting
invitee count where possible.

## 6. Record learning

After the event, capture changes that should affect the next occurrence. Keep
the reusable workflow separate from one week's temporary details.

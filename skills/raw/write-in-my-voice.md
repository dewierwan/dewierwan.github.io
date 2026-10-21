---
name: write-in-my-voice
description: Drafts or revises email in your own voice from real samples, with facts and commitments checked. Use when you say "write this email," "reply to this thread," or "polish my draft."
---

# Write in my voice

Use this workflow when you want an AI assistant to write, reply to, revise, or polish an email. The goal is a concise, copy-ready message that sounds like you while staying accurate, appropriate, and within your authority.

## Quick version

- Paste three to five emails you actually sent recently, plus any style rules (greeting, sign-off, words you avoid), and ask the assistant to summarize your voice before drafting.
- Give a short brief: who the recipient is, what you want the email to achieve, and any facts, dates, or links that must appear.
- Ask for the smallest complete message: purpose or answer in the first sentence, then only the context and next step the recipient needs.
- Tell the assistant not to invent availability, prices, decisions, promises, or feelings, and to ask one question if a missing fact matters.
- Have it check the draft against your voice and your known dislikes, then return only the email, ready to copy.
- Review and send it yourself.

## 1. Load the voice profile

Before drafting, read the user's current writing profile in full, if one is available. A profile may include examples of sent emails, a style guide, approved reusable wording, and a fact bank.

Build or confirm these settings:

| Voice element | What to identify |
|---|---|
| Greeting and sign-off | The user's usual opening, closing, and name format. |
| Tone | Their normal balance of casualness, warmth, directness, and formality. |
| Structure | Typical sentence length, paragraph length, use of bullets, and first-sentence pattern. |
| Language | Preferred contractions, recurring phrases, punctuation habits, and useful colloquialisms. |
| Avoidances | Words, filler, emojis, formatting, or tones the user does not use. |
| Approved material | Current facts, links, scheduling options, boilerplate, and standard replies the user has authorized. |

Use recent, genuinely sent messages as stronger evidence than older examples. If examples conflict, use the most recent consistent pattern or ask the user which preference is current.

A short profile might look like this (invented example):

> Greeting: "Hi [first name]," never last names. Sign-off: "Thanks, Sam." Length: usually two to four sentences. Tone: friendly, direct, contractions welcome. Avoid: emojis, "I hope this finds you well," long apologies, heavy dash use. Fact bank: booking link for intro calls, standard reply for speaking requests.

Do not access private messages, records, or mailboxes unless the user has a legitimate purpose and has clearly authorized access. Read only the minimum relevant messages, omit unrelated or sensitive personal details from the draft and response, and keep the output within the conversation or system the user intended.

## 2. Establish the email brief

Identify the minimum information needed to write safely:

1. Who is the recipient, and what is their relationship to the user?
2. What result should the email produce?
3. Is this a new message, a reply, a follow-up, or a revision?
4. What facts, dates, names, links, attachments, decisions, or commitments must appear?
5. What tone is appropriate: routine, warm, firm, sensitive, urgent, or formal?
6. Is there a deadline, approval boundary, or issue that needs careful wording?

If a missing fact would change the message or create a commitment, ask one focused question. Do not invent availability, decisions, prices, timelines, recipient context, opinions, emotional reactions, or promises.

## 3. Adapt voice to the situation

Keep the user recognizable, but do not treat voice as a rigid template.

- For familiar contacts, follow the user's ordinary level of brevity and informality.
- For new, external, senior, or sensitive recipients, keep the user's voice while making context and requests clearer.
- For corrections, refusals, conflict, or delays, state the relevant facts and next step plainly. Avoid defensiveness, hollow praise, and excessive apology.
- For requests, make the requested action, responsible party, and timing easy to identify.
- Use an approved reusable response, link, or fact when it fits the current context, rather than inventing one. Never reuse material that is stale, misleading, or unauthorized.

## 4. Draft the smallest complete message

Use the user's established greeting and sign-off when appropriate. If no evidence exists, use a broadly useful default: warm-professional, direct, concise, and conventional.

A reliable structure is:

1. Greeting, if useful.
2. The purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, if appropriate.

Prefer active verbs, concrete language, short sentences, and short paragraphs. Use bullets only when they make actions, choices, or logistics easier to scan. If the user dislikes emojis, convert them to plain punctuation or remove them.

Remove material that does not help the recipient act or understand:

- Generic openings or filler.
- Process explanations about drafting or internal work.
- Repeated thanks, praise, or apologies.
- Hedges that weaken a clear statement.
- Unnecessary context and unsupported claims.

Invented example, using the profile above. Brief: a partner at Larkfield Design asked for an intro call; Sam is happy to talk.

> Hi Priya,
>
> Happy to chat! Grab any open slot here: [booking link from fact bank].
>
> Thanks, Sam

## 5. Audit before delivery

Review the draft line by line:

- Does it plausibly sound like the user?
- Do the greeting, sign-off, punctuation, and rhythm match the available evidence?
- Is the level of warmth and formality right for this recipient and situation?
- Are all names, dates, links, attachments, references, and thread details accurate?
- Did the draft add any commitment, factual claim, decision, or emotion not supplied by the user?
- Is the requested action or decision unmistakable?
- Can any sentence be removed without reducing usefulness?
- Does the draft avoid the user's known style anti-patterns?

If no voice evidence exists, state the assumption briefly only when helpful, then provide the draft. Invite the user to share a few representative sent emails or preferences for future work.

## 6. Deliver the draft

By default, provide only the copy-ready email in chat. Do not add explanation after it unless the user asks for options, rationale, or edits.

Only create a draft inside an email system when the user explicitly asks for it (see Optional extras). The user remains responsible for reviewing and sending the message unless they explicitly authorize a separate sending action and the system's permissions and policies allow it.

## Optional extras

### Creating a reviewable draft in an email system

For assistants with connected tools, when the user explicitly asks for a draft in their email system:

1. Confirm authorization to use that system and the intended account or workspace when necessary.
2. Follow the user's applicable email-system policies, including which method is approved. Some setups allow drafting only through the regular web interface (for example, with a browser-control capability) and block direct programmatic draft or send tools. Never work around a blocked method.
3. For a reply, open the original conversation, choose Reply or Reply all as appropriate, type the body, and keep the existing subject unchanged so the draft stays in the same thread.
4. Before finishing, read back the recipients and body to confirm they match what the user approved and that the draft sits in the intended conversation.
5. Leave the draft unsent.
6. Give the user a safe way to open the draft for review and final sending, such as a link to the conversation, without exposing unnecessary account or message data.

### Maintaining the profile

Keep the voice profile and fact bank in one place the user controls. When the user corrects a draft in a way that reflects a lasting preference, suggest adding it to the profile. Review approved facts and links periodically (an adjustable default is every few months) so stale details are not reused.

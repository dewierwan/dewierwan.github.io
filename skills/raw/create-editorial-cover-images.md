---
name: create-editorial-cover-images
description: Create, inspect, and refine eight article-specific editorial cover images using a chosen image generator and an evidence-based two-round workflow.
---

# Create editorial cover images

Turn an article into eight finished editorial cover-image options. Develop five distinct concepts, generate and inspect every result, then create three improved options based on what the rendered images reveal. The goal is a set of comparable images that clearly belong to the article, rather than a set of generic prompts or minor variations on one scene.

This workflow is tool-independent. Use the user’s chosen image-generation system and the confirmed requirements of the intended publishing destination. If the user explicitly asks for prompts only, follow the prompt-only branch instead of generating images.

## Purpose, authorization, and boundaries

Use this workflow when there is a legitimate purpose to create artwork for an article, newsletter, essay, report, or similar editorial work. If the material is unpublished, private, or contains information about people, confirm that the requester is authorized to use it for this purpose.

Use the minimum source material needed to understand the article and create a visual brief. Do not send a full unpublished draft to an external generator unless that is necessary, authorized, and consistent with the user’s privacy expectations. Prefer a distilled, article-specific visual description. Omit unrelated names, private details, confidential facts, and sensitive personal information.

Do not invent events, identities, locations, or biographical claims that the article does not support. A visual metaphor may interpret the article’s idea, but it should not look like a factual depiction of something that did not occur. Respect consent, access, payment, rate-limit, and approval boundaries. If the selected generator is unavailable or blocked, report the exact blocker and ask for the smallest necessary action. Do not bypass a rejection, access control, or approval gate. Do not move content to another service without the user’s agreement.

## Default deliverable and modes

The default deliverable is eight completed images:

1. Five deliberately different first-round concepts.
2. A visual review of all five rendered images.
3. Three second-round images informed by visible strengths, weaknesses, and gaps.

Keep the first five available while creating the final three so the user can compare original concepts with refinements. Give every option a stable number and short title. Use separate jobs, conversations, files, or output locations when the chosen generator supports that arrangement.

Use prompts only when the user explicitly requests prompts, or when image generation is unavailable and the user chooses prompt delivery instead. Do not silently substitute written prompts for requested finished images.

## Establish the brief

Read the complete article before developing concepts. A title alone rarely contains enough information to produce an image that feels specific to the piece. If the article is missing, ask for the copy or an authorized synopsis with enough detail to identify its central idea and tone.

Create a private working brief with these elements:

- **Central move:** the main idea, tension, insight, or change in perspective the reader should take away.
- **Emotional progression:** where the article is quiet, tense, reflective, hopeful, urgent, defiant, or resolved.
- **Concrete visual material:** images, actions, objects, settings, analogies, and metaphors already present in the writing.
- **Tone:** the voice and emotional register that should constrain the visual treatment.
- **Audience and placement:** where the image will appear and how it will be viewed, such as a wide header, social card, presentation cover, printed page, or square preview.

Use this analysis to improve the work. Do not automatically summarize it back to the user unless an explanation would help them make a meaningful creative decision.

Reuse preferences already given in the conversation. Ask only for missing choices that would materially change the image. Collect all outstanding answers before treating a partial reply as the final brief.

When needed, ask these related questions together:

- **Mood:** Offer three or four interpretations tied to specific beats in the article. For example, distinguish a quiet recognition early in the piece from a later moment of momentum or resolve. Do not present abstract mood labels without saying what each interpretation emphasizes.
- **Subject:** Offer suitable choices such as a human presence, landscape, single symbolic object, built environment, or abstract composition. Respect restrictions on likenesses, people, places, or representations.
- **Palette:** Offer palettes that support the selected mood. Name colors, contrast, and lightness so the choice does not depend only on color labels. Do not use color pairs that may be difficult to distinguish as the only difference between options.
- **Orientation and placement:** Confirm the crop or aspect ratio required by the destination. A wide header, square card, and portrait cover need different compositions. Use user-provided or verified requirements instead of assuming a standard ratio.
- **Medium or style:** Establish whether the image should be photographic, painted, drawn, collaged, graphic, or another approach when the request leaves this open.

Keep the agreed brief through both rounds. It should include mood, subject rules, palette, style, format, destination, and chosen generator. Do not ask the same questions again during ordinary iteration.

## Propose five distinct concepts

Present exactly five concepts in a numbered list. Each concept must contain:

1. A short title.
2. A one- to three-sentence description of what the viewer sees.
3. A brief statement of the article idea or emotional beat it expresses.

The five ideas must differ meaningfully in subject, composition, action, metaphor, and emotional emphasis. Five slight changes to the same scene are not a useful comparison set. Unless the user’s restrictions rule them out, include at least one landscape-only option and one single-object or symbolic option. A non-identifying human figure can be useful when human presence matters without portraying a particular person, but it is one option rather than a default.

Apply this test to every concept: could its explanation fit almost any article on the same broad subject? If so, make it more specific to this article or replace it.

Give a one-line initial recommendation, then generate all five when completed images are requested. Do not require the user to select one concept before the first round unless they explicitly want to narrow the scope. The rendered results are the evidence needed for informed comparison.

## Write effective visual prompts

Write one self-contained prompt for each concept. Include enough detail to produce a coherent image, but do not pile together incompatible instructions. Use this structure, combining sections only when doing so improves clarity:

```text
Create one image: [medium, dimensions or aspect ratio, and overall editorial character].

Subject: [what is visible, its action, scale, prominence, and position. Include relevant constraints here, such as no visible facial detail, no logos, or no lettering].

Setting: [surroundings, depth, foreground and background relationships, or environmental context].

Light and palette: [direction and quality of light, specifically named colors, contrast, and transitions].

Technique: [visible properties of the chosen medium, edge treatment, texture, detail level, and negative space].

Mood: [the intended feeling and its connection to the article’s central move].

Composition: [focal point, eye path, major shape placement, crop, aspect ratio, and any reserved empty space].

Avoid: [artifacts, conventions, or content that conflict with the brief].
```

Name colors and their relationships rather than relying only on vague terms such as “warm,” “cinematic,” or “moody.” For example, “pale ochre ground fading into blue-grey shadow, with a small muted violet accent” is more actionable than “dramatic warm light.” Choose the palette from the article and the user’s preferences, not from a permanent aesthetic default.

Describe the chosen medium through its actual visual qualities. Watercolor may need wet-on-wet washes, pigment blooms, paper texture, transparent glazing, selective edges, and unpainted space. Charcoal may need broad tonal masses, broken edges, and paper grain. Photography may need a plausible light direction, lens distance, depth of field, and realistic materials. Avoid instructions that conflict with one another.

Put important exclusions alongside relevant positive instructions as well as in the final Avoid section. For example, state “silhouette with no visible facial detail” in the subject section if anonymity matters. Establish whether typography will be added later. Unless text is intentional, request no text, logos, borders, or watermarks.

Send only the visual brief required for the individual image. Use article-specific facts only when supported by the source and appropriate to visualize.

## Generate the first five

Use the chosen generator’s supported workflow. Explicitly request creation of one image so that a text response is not mistaken for an image deliverable. Adapt syntax to the service while preserving the concept, composition, palette, format, and exclusions.

Maintain a working record for every option: number, title, concept, submitted prompt, generation status, output location, and review notes. Preserve the complete prompt so a truncated or failed request can be repaired accurately.

For browser-based or session-based generators, use these general checks:

1. Create distinct, clearly identifiable jobs or conversations for options one through five. Do not take over unrelated user work.
2. Confirm that the complete prompt appears in the live submission interface before sending it.
3. Verify that the service accepted the intended request.
4. Record only observed links, session locations, or identifiers. Never invent output locations.
5. Start independent jobs without unnecessary delay when the tool supports it, while keeping interface actions sequential and grounded in the current page state.
6. Confirm completion by opening the actual rendered image at a useful size. A spinner, placeholder, accepted request, elapsed time, or text description is not proof of completion.
7. If an error appears, first check whether an image already completed before retrying, to avoid duplicates and wasted quota.

If a service responds with text instead of an image, request image generation again in the same job when possible. Keep unsuccessful attempts separate from completed options.

## Inspect all five before improving

View every first-round image at a useful size. Evaluate rendered pixels, not the generator’s description and not the original intention. Also inspect a reduced preview, because editorial cover art must communicate when small or cropped.

For each image, assess:

- Whether it communicates the article’s central idea and emotional tone.
- Whether the subject, action, and focal point read immediately.
- Whether the requested style, palette, orientation, and composition survived generation.
- Whether it is too busy, generic, sentimental, static, literal, decorative, or confusing.
- Whether anatomy, objects, perspective, structure, texture, or unintended lettering contain visible artifacts.
- Whether it remains distinct from the other options and useful as editorial cover art.

Only after inspecting all five should you write the three second-round prompts. Each must respond to visible evidence: preserve a demonstrated strength, correct a specific weakness, or fill a meaningful conceptual gap. Do not prewrite this round before visual review.

A useful second round often includes one refinement of the strongest first-round result, one synthesis of strengths from different images, and one new concept that addresses an unmet need. Treat this as a guide rather than a rigid formula.

Fix causes instead of adding decoration. If an image is cluttered, reduce objects, competing focal points, or scene complexity. If a painting resembles a photograph with a superficial filter, specify larger shapes, selective edges, authentic marks, and more negative space. If a scene feels like generic stock imagery, revisit the action or metaphor before adding detail.

Give a short progress update describing what the first images revealed and what the next three will improve. Continue without requesting another creative selection unless a new decision is genuinely required.

## Generate, review, and deliver options six through eight

Generate three new images from the evidence-based prompts. Keep options one through five unchanged. Inspect every second-round image using the same completion and visual-review criteria. Repair failures where possible, but do not count a failed request, text-only response, or reused old image as a completed new option.

Before delivery, verify:

- Eight distinct completed outputs exist.
- Each finished image was personally inspected.
- Each option can be opened from the final handoff location.
- Numbering, titles, and output locations match the working record.
- Options six through eight are clearly marked as the second round.
- Outputs remain within the user’s authorized access boundary.

Leave outputs available in the form the user requested, such as open sessions, a generator gallery, or verified download locations. Do not create an unnecessary separate document or gallery when native generator outputs are sufficient for comparison.

Recommend the strongest rendered option in one short sentence, explaining why it fits the article. Then provide a numbered list of all eight titles and verified output locations, clearly marking the second-round options. Make that list the final deliverable block. If fewer than eight images are complete because of access limits, rate limits, or persistent errors, state exactly which options are finished and which remain blocked. Preserve useful work for resumption and never represent prompts as completed images.

## Prompt-only branch

When the user explicitly requests prompts only, do not generate images. Read the article, establish the same creative brief, and propose five concepts. Wait for a selection unless the user already selected concepts or asked for prompts for all five.

Write every selected prompt in a separate fenced code block using the prompt structure above. If combining concepts, add one brief sentence explaining what is being combined. Do not call later prompts visual improvements, because no first-round images were inspected. Put the selected prompts last, with nothing after the final prompt block.

## Adapt to another image generator

When creating a variant for another generator, preserve the underlying concept, mood, composition, palette, aspect ratio, and exclusions. Change only the syntax, controls, and prompt structure needed by the target service.

Use prose for tools that work best with full visual descriptions. Use concise descriptive phrases and documented parameters only for tools that support them. Check current tool conventions before including version flags, style controls, seeds, or aspect-ratio syntax. If a setting materially affects the result and remains unclear, ask once rather than guessing.

A platform variant is not a new visual concept. Keep the image idea consistent so the user can compare tools fairly.

## Learning and quality audit

After the user chooses an image, accepts a prompt, or clearly ends iteration, retain only durable lessons that the user has authorized to be remembered. Useful lessons may concern article interpretation, composition, prompt constraints, medium direction, or verified generator behavior. Distinguish explicit user feedback from personal aesthetic inference.

Do not retain private article content, unpublished facts, personal details, or one-off subject matter as reusable guidance. Do not turn one successful composition into a universal default. If no general lesson emerged, make no workflow change.

Before considering the task complete, audit the work:

- Was the full article, or an authorized sufficient brief, read before concept development?
- Were mood, subject, palette, style, orientation, destination, and generator resolved or intentionally left open?
- Are the five first-round concepts genuinely distinct and grounded in article-specific beats?
- Does every prompt contain a clear subject, composition, palette, technique, format, and relevant exclusions?
- Were all first-round images inspected before the second-round prompts were written?
- Does each second-round prompt respond to visible evidence rather than a preplanned variation?
- Were eight distinct completed images verified, or were incomplete results reported honestly?
- Were privacy, authorization, access, and approval boundaries respected throughout?

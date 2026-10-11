---
name: create-editorial-cover-images
description: Create and review eight article-specific cover-image options through five initial concepts and three evidence-based improvements.
---

# Create editorial cover images

Turn a written article into eight finished editorial cover-image options. Develop five genuinely different first-round concepts, generate and inspect each rendered result, then create three new options based on what the first round actually revealed. The user should receive finished, accessible images that clearly relate to the article, not merely a list of hypothetical prompts.

Use the user’s chosen image generator, publication destination, medium, and approved access method. Do not assume a particular service, account, browser, house style, or aspect ratio. If the user explicitly requests prompts only, follow the prompt-only branch.

## Purpose, authorization, and readiness

A cover image should do more than decorate a topic. It should express the article’s central move, emotional register, or defining metaphor in a form that still communicates at thumbnail size.

Before generating, confirm the following:

- You have the complete article or the minimum necessary excerpts. Do not create article-specific concepts from a title alone unless the user explicitly accepts a broad interpretation.
- You have a legitimate purpose and clear authorization to use unpublished, private, or sensitive material. Use only the information needed for the visual brief.
- The image generator and intended destination are clear. If the chosen service is unavailable, report the blocker and ask before moving article material or prompts to a different service.
- The intended placement, crop, and output format are known or can be selected with the user.
- Restrictions about people, places, brands, factual depiction, lettering, source material, or sensitive content are known.

Do not paste a full unpublished article into an image generator by default. Extract only the visual facts, metaphors, and tone needed for the prompt. Omit unrelated personal details, identifying information, sensitive claims, and private context. Do not imply that an imagined scene documents a real event unless the source supports that depiction and the user wants a factual depiction.

If the article copy is absent, ask for it before proceeding. If only a summary is available, explain that the image will be based on the summary rather than a full reading.

## Establish the creative brief

Read the article end to end before proposing images. Identify these elements internally:

- **Central move:** the idea, tension, realization, or change in perspective the reader should retain.
- **Emotional progression:** where the writing becomes quiet, accelerates, turns, becomes uncertain, or resolves.
- **Concrete source imagery:** objects, places, actions, comparisons, and metaphors already present in the article.
- **Tone:** for example, reflective, investigative, urgent, hopeful, defiant, celebratory, or sober.
- **Editorial constraints:** what must not be shown, what could be misread, and whether a literal depiction would be misleading.

Use this analysis to make decisions. Do not automatically return a long summary of the article. Never invent facts about the article. Every concept must be grounded in the source or clearly framed as a visual interpretation.

Reuse preferences already stated in the conversation. Ask only for missing choices that materially affect the output, and collect all outstanding answers before treating a partial response as a complete brief. Make the options specific to this article rather than using generic design-menu labels.

Ask about these four areas when needed:

1. **Mood:** Offer three or four valid readings of this particular article. Link each option to a distinct emotional beat or argument in the piece.
2. **Subject:** Offer fitting choices such as an anonymous figure, landscape only, a single symbolic object, an architectural or environmental scene, or an abstract composition. Respect restrictions on depicting people or real places.
3. **Palette:** Offer palettes with named colors, value range, and contrast character. Describe alternatives in ways that do not depend only on distinguishing color labels.
4. **Orientation:** Confirm the intended placement: wide header, square preview, portrait cover, or a supplied custom ratio. Verify destination requirements when possible rather than carrying over dimensions from another publication.

Also establish the medium or visual style if it remains open. Useful choices include documentary photography, watercolor, ink drawing, collage, printmaking, restrained three-dimensional illustration, or abstract painting. Select a style according to the article and audience, not an unstated personal preference.

Keep a compact working brief containing the central move, selected mood, subject constraints, palette, medium, orientation, generator, and exclusions. Carry this brief through both rounds without repeatedly asking the same questions.

## Develop five distinct concepts

Present exactly five first-round concepts. For each, provide:

1. A short title.
2. A one- to three-sentence description of what the viewer sees.
3. A short statement of the article beat, argument, or emotion the concept expresses.

Give a one-line initial recommendation, then generate all five when finished images are requested. Do not ask the user to select a concept before the first round unless they explicitly request that gate.

The concepts must differ in subject, composition, visual metaphor, and emotional emphasis. Five variations of the same person in the same setting are not meaningful options. Unless the brief rules them out, include at least one landscape-only concept and one single-object or symbolic concept. Anonymous figures can be useful when universality matters, but they are not required.

Use this test before retaining a concept: could the same explanation fit almost any article on the topic? If yes, replace it with an interpretation tied more directly to this article’s argument, image, or emotional turn.

## Write effective visual prompts

Write one self-contained prompt per concept. Explicitly request an image so the generator does not return text or a revised prompt. Adapt formatting to the target generator’s documented capabilities while preserving the visual logic.

Use this structure, combining sections only where that makes the prompt clearer:

```text
Create one image: [medium, overall editorial character, and requested format].

Subject: [what is in frame, where it appears, what it is doing, scale and prominence. Place relevant exclusions here, such as no recognizable face, no logos, or no text.]

Setting: [surroundings, depth, foreground and background relationships, and what recedes or remains empty.]

Light and palette: [specific colors, their transitions, light direction, contrast, and atmosphere.]

Technique: [physical or visual properties of the selected medium, texture, edge treatment, level of detail, and negative space.]

Mood: [the feeling and its link to the article’s central move.]

Composition: [focal point, eye path, placement of major shapes, crop, negative space, and aspect ratio.]

Avoid: [only artifacts, visual conventions, or content that conflicts with the brief.]
```

Name colors precisely. “Pale ochre ground, slate-blue shadows, faded apricot light, and a deep violet horizon” is more actionable than “warm and moody.” Specify how colors relate, where transitions occur, and how saturated they should be.

Describe the actual characteristics of the medium. For watercolor, useful direction may include broad wet-on-wet washes, pigment blooms, visible paper grain, transparent layers, selective edges, and unpainted paper. For photography, describe lighting, distance or depth cues, and realism level instead. Do not ask for photographic sharpness and loose, minimal watercolor marks in the same area without a clear reason.

Put important exclusions near the relevant positive instruction as well as in the final avoidance line. For example, say “a back-turned silhouette with no visible facial features” in the subject description. Avoid unintended lettering, logos, watermarks, borders, and interface-like artifacts unless the user specifically requests them.

## Generate the first five

Use the selected generator through an authorized method that respects its available controls and the user’s access boundary. Respect spending limits, consent expectations, and approval gates. Do not bypass a login, approval request, rate limit, or access restriction. If the service is blocked, state what is blocked, preserve completed work where possible, and ask only for the action needed to resume.

Maintain a working record for each option: number, title, concept, full submitted prompt, status, verified output location, and visual-review notes. This prevents prompt loss, inconsistent numbering, and accidental substitution of unfinished output.

For each submission:

1. Create a separate, clearly distinguishable generation context when the generator supports it.
2. Enter the complete prompt and verify that the visible input contains the intended text before sending.
3. Request one image now, rather than a prompt, explanation, or textual response.
4. Confirm the request was accepted with the complete prompt.
5. Confirm that a rendered image exists and can be opened at useful size.

An accepted message, spinner, placeholder, elapsed time, thumbnail shell, or model description is not proof of completion. Inspect loaded image pixels. If an error appears, first check whether an image already completed before retrying, so unnecessary duplicates are not created. Keep failed attempts separate from finished options.

Independent jobs may run concurrently when the generator safely supports that pattern. Keep interactions with a shared interface sequential and based on the current visible state.

## Inspect all five before making improvements

View every first-round image at useful size. Judge the rendered result, not the generator’s claims or the prompt’s intended result. Also inspect each image at approximate cover-thumbnail size.

For each option, assess:

- Does it communicate the central idea and emotional tone?
- Is the focal subject or action immediately understandable?
- Did the requested medium, palette, shape, and composition survive generation?
- Is it too busy, generic, sentimental, static, literal, or visually confusing?
- Are there visible anatomy, perspective, object, construction, lettering, or artifact problems?
- Does it still work after cropping or reduction?

Only after reviewing all five should you design options six through eight. For each new prompt, record the observed strength to keep, the weakness to correct, and the visible change expected to help.

A useful second-round spread is a refinement of the strongest first-round image, a combination of strengths from different images, and a new direction that addresses a gap in the first round. Use judgment rather than forcing this pattern. The goal is a stronger range, not mechanical compliance.

Fix causes rather than symptoms. When a scene is cluttered, remove competing objects or simplify the action before adding decorative detail. When an image resembles a photograph with a painted filter, request fewer large forms, selective edges, meaningful negative space, and the actual marks of the chosen medium. When a result feels like generic travel, office, or lifestyle imagery, reconsider the metaphor or point of view rather than adding more props.

Give the user a short progress update describing what the rendered images revealed and what the next three will improve. Do not ask for another selection unless the user requests one.

## Generate, inspect, and hand off options six through eight

Generate three distinct second-round images using the revised prompts. Preserve the first five unchanged for comparison. Apply the same submission, completion, and visual-inspection checks to each new image.

If a generation fails or returns text only, repair it in the same generation context where possible. Do not count unsuccessful requests as finished options, and do not silently substitute an old image. If a rate limit or access gate prevents completion, say exactly which options are complete and which remain blocked.

Before delivery, pass this readiness gate:

- There are eight distinct completed images, not eight prompts or placeholders.
- Each image was inspected at useful size.
- Each output can be opened from its final handoff location.
- Titles, numbers, links or file references, and review notes match.
- Options six through eight are clearly marked as second-round options.
- The user can access the images within the authorized sharing boundary.

Recommend the strongest rendered image in one short sentence based on the actual visual result. Then provide a numbered list of all eight titles and verified output locations, marking the final three as second-round options. Make that list the final deliverable block. Do not claim completion when some outputs are failed, inaccessible, or uninspected.

## Prompt-only branch

When the user explicitly asks for prompts only, do not generate images. Read the article, establish the needed preferences, and propose five concepts. Wait for a selection unless the user already selected concepts or asked for all prompts.

Deliver each selected prompt in its own fenced code block using the prompt structure above. If combining concepts, give one brief sentence explaining the combination immediately before the prompt. Do not invent a visually informed second round when no images were generated and reviewed. Put the selected prompts last, with nothing after the final code block.

## Adapt to another generator

When creating a version for another generator, preserve the core subject, composition, palette, mood, exclusions, and format. Change only the syntax and controls required by the target tool.

Check current supported conventions before using parameter flags, model versions, or aspect-ratio controls. If a version is necessary and unclear, ask once rather than guessing. Keep platform-specific variants separate and labeled. A change in generator should not quietly become a different creative concept.

## Learn from outcomes

After the user selects an image, accepts a prompt, or gives clear feedback, capture only durable, authorized lessons. Useful lessons include a recurring preference for sparse compositions, a prompt constraint that prevented a common artifact, or a verified convention of an approved generator.

Distinguish explicit user feedback from your own aesthetic judgment. Do not retain private article content, identifying facts, sensitive details, access information, or one-off subject matter as reusable defaults. Do not alter the workflow when a run revealed no general lesson.

---
name: create-editorial-cover-images
description: Create eight article-grounded cover-image options through five concepts, visual review, and three evidence-based improvements in any chosen image generator.
---

# Create editorial cover images

Turn an article into eight finished editorial cover-image options. Develop five distinct concepts, generate and inspect every result, then create three improvements based on what the rendered images actually reveal. The user chooses from finished images that have a clear, honest connection to the article.

Use the user's chosen image generator, publishing destination, and delivery method. Do not assume a particular service, account, medium, aspect ratio, palette, or visual aesthetic. If the user explicitly requests prompts only, use the prompt-only branch rather than generating images.

## Purpose, authorization, and boundaries

Work from the complete article, not from a title alone. If the article is unpublished, confidential, or includes personal information, confirm that the user is authorized to use it for this purpose. Send only the minimum visual brief required to the selected generator. Do not paste full unpublished copy, private correspondence, sensitive facts, unrelated names, or identifying details unless they are necessary to the image and the user has clearly authorized their use.

Do not invent scenes, events, identities, or claims that the article does not support. A metaphor may interpret an idea, but it should not falsely present a real event as a factual depiction. Respect access controls, account permissions, spending limits, approval gates, consent expectations, and the intended audience for the final image.

## Establish the brief

Read the article from beginning to end before creating concepts. If the copy is missing, request it before generating. A title rarely provides enough information to create an image that belongs specifically to the piece.

Identify the following internally and use them to guide the work:

- **Central move:** the idea, shift in perspective, or conclusion a reader should retain.
- **Emotional progression:** where the piece is quiet, tense, hopeful, defiant, reflective, or resolved.
- **Concrete source material:** images, actions, settings, symbols, and metaphors already present in the writing.
- **Tone:** the article's voice and level of seriousness, intimacy, energy, or restraint.
- **Publication context:** where the image will appear, how small it may be displayed, and whether later typography will be added.

Do not begin with a long summary unless the user requests one. Translate this understanding into visual choices instead.

Reuse preferences already supplied in the conversation. Ask only for missing choices that would materially change the image. Group related questions together and collect all outstanding answers before treating a partial response as the complete brief.

Ask about these areas when they remain unclear:

- **Mood:** Offer three or four interpretations tied to actual beats in the article. For example, distinguish a contemplative opening from a more forward-moving conclusion rather than offering generic labels alone.
- **Subject:** Establish whether the image should use a human figure, landscape, symbolic object, abstract composition, or another article-appropriate subject. Respect restrictions about faces, bodies, places, cultural references, or factual depictions.
- **Palette:** Offer a small set of palettes appropriate to the mood. Name specific colors and describe contrast, value, and lightness so the choice does not depend only on color labels.
- **Orientation and crop:** Determine the intended placement: wide header, social preview, square tile, portrait cover, or a user-supplied dimension. Verify the destination's requirements when possible rather than assuming a universal ratio.
- **Medium or style:** Establish photography, watercolor, ink, collage, charcoal, digital painting, or another treatment if the user has not already specified one.

Keep a short working brief with the confirmed format, generator, mood, subject constraints, palette, medium, and any required empty space for text. Carry this brief through both rounds without repeatedly asking the same questions.

## Propose five distinct concepts

Present exactly five initial concepts in a numbered list. Each concept must include:

1. A short title.
2. A one- to three-sentence description of what the viewer sees.
3. A brief statement of the article idea or emotional beat it expresses.

The five concepts must differ in subject, composition, visual metaphor, or emotional emphasis. Five minor variations on the same scene are not a useful range. Unless user constraints rule them out, include at least one landscape-only option and one single-object or symbolic option. A human figure can be effective, but it should serve the article rather than become an automatic default.

For every concept, ask: could this image reasonably accompany many unrelated articles on the same topic? If yes, replace it with something more grounded in this article's actual language, movement, or insight.

Give a one-line initial recommendation, then generate all five concepts when finished images are requested. Do not make the user choose before the first visual round unless they explicitly ask to select concepts first.

## Write effective visual prompts

Write one self-contained prompt per concept. The prompt should be precise enough to render, but should not pile up competing instructions. Use the following structure, merging sections only when doing so improves clarity:

```text
Create one image: [medium, format, and overall editorial character].

Subject: [what is visible, what it is doing, its prominence and position. Put relevant exclusions here, such as no visible face, no logo, or no lettering.]

Setting: [surroundings, depth, foreground and background relationships, and what recedes from view.]

Light and palette: [time of day or light direction, named colors, contrast, and visible color transitions.]

Technique: [the medium's actual marks, texture, edge treatment, level of detail, and use of negative space.]

Mood: [the feeling and its connection to the article's central move.]

Composition: [focal point, eye path, placement of major forms, crop, aspect ratio, and reserved space if needed.]

Avoid: [only artifacts, visual conventions, or content that conflict with the brief.]
```

Name colors and their relationships rather than relying on vague directions such as “warm” or “moody.” For example, “pale ochre ground against muted violet shadows and a cool blue-gray horizon” gives more useful direction than “dramatic golden-hour light.” Use palette examples to make the selected direction concrete, not to impose a fixed palette on every assignment.

Describe the physical behavior of the chosen medium. Watercolor may need transparent washes, pigment blooms, softened edges, paper texture, and unpainted space. Charcoal may need broad tonal masses, broken edges, and visible tooth of paper. Photography may need lens distance, depth of field, natural light direction, and believable materials. Do not combine incompatible instructions merely because they sound attractive.

Put important exclusions beside the relevant positive instruction as well as in the final avoidance list. For example, say “a back-turned silhouette with no facial detail” in the subject description, not only “avoid faces” at the end. Specify whether the image should contain no text, borders, logos, or watermark-like marks.

Send the generator only the visual prompt needed for that image. Explicitly request that it create an image, so a text explanation is not mistaken for a completed result.

## Generate the first five

Use the chosen generator's supported workflow. If browser or account access is required, use the authorized account and current supported controls. Do not take over unrelated workspaces or conversations. If access is unavailable, an approval gate blocks action, or a rate limit applies, report the blocker and ask for only the action needed to continue. Do not silently send the article to another service as a substitute.

Maintain a working record for each option: number, title, concept, full submitted prompt, generation status, output location, and visual-review notes. Preserve the exact prompt so a truncated or failed request can be repaired accurately.

Independent jobs may be started without waiting for each image to finish when the tool supports this safely. Keep browser actions sequential, grounded in the current page state, and within the generator's limits. Confirm that each submission contains the complete intended prompt. If text is cut off, cancel or correct the incomplete attempt and resend the complete brief.

A submitted prompt, spinner, thumbnail placeholder, elapsed time, or text response is not proof of completion. Confirm that a real image has rendered and can be opened at useful size. If an error appears, check whether an image was nonetheless completed before retrying, to avoid duplicate output. Keep unsuccessful attempts separate from the five finished options.

## Inspect all five before improving

View every completed image at useful size. Evaluate the actual pixels, not the generator's description or the intended prompt. Also inspect a small preview or reduced crop, because editorial covers often need to communicate quickly at thumbnail size.

For each option, assess:

- Whether it communicates the central idea and emotional tone.
- Whether the subject and action read immediately and have a clear focal point.
- Whether the requested style, palette, orientation, and composition survived generation.
- Whether it feels too busy, generic, sentimental, static, overly literal, or visually confusing.
- Whether anatomy, objects, perspective, construction, lettering, or other visible artifacts undermine it.

Only after all five have been inspected, write three new prompts. Each improved prompt must name, in working notes, a visible strength to retain, a weakness to correct, and a concrete visual change likely to help. Do not prewrite the second round before reviewing the first results.

A useful second-round spread is often: one refinement of the strongest result, one combination of strengths from different results, and one new concept that addresses an uncovered gap. This is a guide, not a rigid formula. Choose another distribution if it better serves the article.

Correct causes rather than decorating symptoms. If an image is cluttered, reduce competing objects and focal points before adding detail. If a painting looks like a photograph with a filter applied, request fewer large forms, selective edges, visible medium marks, and more negative space. If a scene reads as generic travel, business, or lifestyle imagery, reconsider the action or metaphor instead of adding ornamental detail.

Give the user a short progress update on what the first round revealed and what the next three will improve. Continue without asking for another selection unless the user requests a pause.

## Generate, review, and deliver options six through eight

Generate three images from the revised prompts. Keep the first five intact so the user can compare originals and improvements. Inspect each new result with the same completion checks and visual criteria. If a generation fails or returns only text, repair it where possible in the same task context. Do not count a failed attempt as a finished option and do not quietly substitute an older image.

Before delivery, verify that there are eight distinct completed images that you personally inspected. Confirm that titles, numbering, prompts, and output locations match the working record. Preserve the final outputs using the generator's supported links, assets, tabs, or files so the user can compare them.

Give a short recommendation based on the rendered work, explaining why the strongest option fits the article. Then provide a numbered list of all eight titles and verified output locations, clearly marking options six through eight as the second round. Make that list the final deliverable block. If output is delivered through browser tabs, leave the finished tabs open and clearly identifiable when the environment supports doing so.

If access restrictions, rate limits, or repeated errors prevent completion, state exactly which options are finished and which are blocked. Preserve useful partial work for resumption. Never claim that eight images exist when some are only prompts, placeholders, or unsuccessful attempts.

## Prompt-only branch

When the user explicitly requests prompts only, do not generate images. Read the article, establish the same creative brief, and propose five concepts. Wait for a selection unless the user already selected concepts or requested prompts for all five.

Write each selected prompt in a separate fenced code block using the prompt structure above. If combining concepts, provide one sentence describing what is being combined before the prompt. Put the selected prompts last, with nothing after the final code block.

Do not describe hypothetical second-round prompts as though they were informed by visual review. No visual review occurred in this branch.

## Adapt to another generator

When the user requests a version for another generator, preserve the core concept, mood, palette, composition, and format. Change only the syntax and structure required by the target tool. A prose-oriented tool may use a compact paragraph, while another tool may work best with short descriptive phrases and supported controls.

Verify current conventions before adding parameter flags, version identifiers, style codes, or aspect-ratio syntax. If a version choice materially affects the result and is unclear, ask once rather than guessing. Keep platform variants separate and clearly labeled. Changing tools should not quietly change the underlying image idea.

## Learn from completed work

After the user chooses an image, accepts a prompt, or clearly ends iteration, identify durable lessons from explicit feedback and observed results. Useful lessons include better ways to translate article structure into a visual metaphor, constrain composition, describe a medium, or avoid a repeated generator failure.

Separate stated user preferences from personal aesthetic judgment. Do not save article-specific names, private content, sensitive facts, or one-off subject matter as a general rule. Do not treat a single successful image as a permanent default. Save or apply a reusable lesson only when the user has authorized memory or workflow updates; otherwise use the lesson only within the current task.

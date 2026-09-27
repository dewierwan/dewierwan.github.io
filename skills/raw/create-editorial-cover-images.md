---
name: create-editorial-cover-images
description: Create eight editorial cover-image options from an article by generating five distinct concepts, reviewing the rendered results, and producing three evidence-based improvements. It supports a user-chosen image generator, format, and visual.
---

# Create editorial cover images

Turn an article into eight finished editorial cover-image options. Develop five genuinely different concepts, generate and inspect each result, then create three additional images informed by what the first round actually revealed. The goal is a set of rendered options that belong to the article, not generic illustrations of its broad topic.

Use the image generator, publication destination, aspect ratio, delivery method, and visual style chosen by the user. Do not assume a particular account, service, browser, medium, or publishing platform. The default deliverable is finished images, not prompts. Use the prompt-only branch only when the user explicitly asks for prompts without generation.

When the source includes unpublished work, private communications, or records about people, proceed only for a legitimate purpose with clear authorization. Use only the minimum relevant material. Do not send unnecessary personal details to an image generator, and keep outputs within the user’s appropriate access and publication boundary.

## Readiness gate

Do not generate from a title alone unless the user explicitly says no further copy exists and accepts a more interpretive result. Ask for the complete article or a sufficient approved excerpt before developing concepts.

Before beginning, establish the following:

- The article or approved excerpt.
- The intended destination and its dimensions or aspect ratio.
- The selected generator and authorization to use it.
- Whether the user wants finished images, prompts only, or a version for a specific generator.
- Any restrictions, such as no people, no faces, no text, no logos, no factual depictions, or required empty space for later typography.

Reuse preferences already provided. Ask only for missing choices that materially change the result, and collect related choices together. Do not repeat the same questions during later rounds.

## Build the visual brief

Read the article end to end. Identify these points internally and use them to direct the images. Do not return a long literary summary unless the user asks for one.

1. **Central move:** The idea, realization, or change in perspective the reader should carry away.
2. **Emotional progression:** Where the article opens, shifts, intensifies, quietens, or resolves.
3. **Concrete imagery:** Objects, settings, actions, metaphors, and visual language already present in the writing.
4. **Voice and register:** For example, reflective, urgent, skeptical, hopeful, sober, intimate, or celebratory.
5. **Factual boundaries:** Details that may be shown literally and details that should remain abstract, omitted, or clearly metaphorical.

Do not invent facts, identities, events, or locations unsupported by the source. A visual metaphor can be imaginative, but it should not imply that a speculative scene is a factual depiction.

Ask only the unresolved creative questions that would affect the output. Shape answer choices around the actual article rather than using generic menus.

- **Mood:** Offer three or four plausible emotional readings, each tied to a distinct beat in the article.
- **Subject:** Offer appropriate choices such as an anonymous figure, landscape only, a single symbolic object, or abstract composition. Respect stated representation restrictions.
- **Palette:** Offer a few palettes suited to the mood. Describe specific colors plus useful non-color distinctions, such as pale versus dark, muted versus vivid, or low versus high contrast.
- **Orientation:** Confirm the crop and placement, such as wide header, square preview, or portrait cover. Use verified destination requirements when available.
- **Medium or style:** If unspecified, ask whether the user wants photography, painting, ink, collage, graphic abstraction, or another visual language.

Keep a concise working brief with the chosen mood, subject limits, palette, medium, format, generator, and publishing constraints.

## Propose five distinct concepts

Present exactly five numbered image ideas. Each must include:

- A short title.
- A one- to three-sentence description of what the viewer sees.
- A short statement of the article idea or emotional beat it expresses.

The five concepts must differ in subject, composition, and interpretive approach. Five minor variations on the same scene do not create a useful choice set. Unless the user’s restrictions rule them out, include at least one landscape-only option and one single-object or symbolic option.

Test each concept before retaining it: could the same explanation fit nearly any article on this broad topic? If so, replace it with a more article-specific interpretation. Give a one-line initial recommendation, then generate all five when finished images were requested. Do not require concept approval first unless the user asks to approve concepts before generation.

## Write self-contained visual prompts

Write one prompt per concept. Send the generator only the visual material needed to render the image. Do not paste the full unpublished article, private correspondence, or irrelevant details about real people.

Use this structure, combining sections where that improves clarity:

```text
Create one image: [medium, dimensions or aspect ratio, and overall editorial character].

Subject: [what is visible, its action, prominence, position, and relevant exclusions].

Setting: [surroundings, depth, and foreground/background relationships where useful].

Light and palette: [light source, specific colors, contrast, and transitions].

Technique: [physical qualities of the medium, texture, edge treatment, detail level, and negative space].

Mood: [feeling and its connection to the article’s central move].

Composition: [focal point, eye path, arrangement of major shapes, crop, and aspect ratio].

Avoid: [artifacts, content, or conventions that conflict with the brief].
```

Name colors specifically. “Pale ochre, dusty rose, muted blue-grey, and deep violet shadows” gives clearer direction than “warm and moody.” Describe relationships too: whether a dark form sits against a pale field, cool shadows recede, or one restrained accent directs the eye.

Describe the real qualities of the selected medium. Watercolor may require wet-on-wet washes, pigment blooms, visible paper, selective edges, and substantial unpainted space. Charcoal may require broad tonal masses, broken contours, and paper grain. Photography may require lens perspective, depth of field, credible materials, and a defined light source. Do not combine incompatible instructions simply because they sound visually appealing.

Put important exclusions next to the positive instruction as well as in the final avoidance list. For example, say “anonymous silhouette with no facial detail” in the subject description, not only “avoid faces” at the end. Unless lettering is expressly requested and appropriate for the generator, specify no text, logos, borders, watermarks, or unintended signage.

## Generate the first five

Use the chosen generator’s supported workflow. Respect account access, payment, rate-limit, consent, and approval boundaries. Do not bypass an approval gate or access restriction. If the chosen service is unavailable, report the blocker, take only safe recovery steps, and ask whether the user wants to resume later or authorize a specific alternative. Do not send the article to another service without agreement.

Create five distinct generation tasks or conversations where the platform permits. Keep a working record for every option: number, title, concept, submitted prompt, output location, status, and review notes. Preserve the exact prompt so a failed or truncated request can be repaired accurately.

Explicitly request an image. Confirm that the complete intended prompt was submitted, then confirm that an actual image completed and can be viewed at useful size. A text reply, accepted request, elapsed time, thumbnail placeholder, spinner, or progress message is not a finished image.

Start independent requests without waiting for each image only when the tool supports this safely. Keep actions sequential when they share browser focus or a workspace. If an error appears, first check whether an image was already created before retrying. Keep failed attempts separate from completed options.

## Inspect all five before improving

View every rendered image at useful size and evaluate the actual pixels, not the generator’s description or the intended prompt. Also inspect a small preview or intended crop, because a cover must communicate when reduced.

For each option, assess:

- Whether it communicates the central idea and emotional tone.
- Whether the subject or action reads quickly, with a clear focal point.
- Whether the requested medium, palette, dimensions, and composition survived generation.
- Whether it is too busy, generic, sentimental, static, literal, or vague.
- Whether anatomy, objects, perspective, construction, lettering, or rendering show visible errors.
- Whether it still works in the destination crop and thumbnail size.

Only after reviewing all five, write three new prompts. Each should identify an observed strength to retain, a visible weakness to correct, and a visual change likely to improve the result. Do not prewrite the second round before visual review.

A useful spread is often one refinement of the strongest result, one combination of strengths from different images, and one new concept that addresses a gap. Use judgment rather than forcing this pattern. Every new option must be meaningfully informed by rendered evidence.

Fix causes rather than symptoms. If an image is cluttered, reduce objects and competing focal points before adding decoration. If a painting looks like a photograph with a filter, request fewer large shapes, selective edges, and the actual marks of the medium. If a scene feels generic, reconsider the action or metaphor rather than adding detail.

Give a brief progress update explaining what the first round revealed and what the next three images will improve. Continue without requesting another selection or repeating the full brief.

## Generate, inspect, and deliver options six through eight

Generate three new images from the revised prompts. Preserve the first five so the user can compare originals and improvements. Inspect all three using the same completion checks and visual criteria. Repair a failed attempt where practical, but do not count text-only output, an error state, or an unfinished placeholder as a completed option.

Before handoff, verify that eight distinct completed images exist, that each was inspected at useful size, that each can be opened through the agreed delivery method, and that numbering and titles match the working record. Clearly identify options six through eight as the second round. If the platform supports a persistent handoff or preservation action, perform it for every completed output.

Give a short recommendation based on the rendered images. Then provide a numbered list of all eight titles and verified output locations, with the second-round options identified. Keep this list as the final deliverable block.

If access, rate limits, generation failures, or approval gates prevent completion, state exactly which options are finished and which remain blocked. Preserve useful partial work for resumption. Never claim that eight images exist when some are only prompts, placeholders, or unsuccessful attempts.

## Prompt-only branch

When the user explicitly requests prompts only, do not open generation tasks. Read the article, collect the necessary preferences, and propose five concepts. Wait for selection unless the user already selected concepts or asked for all prompts.

Write each selected prompt in its own fenced code block using the prompt structure above. If combining concepts, provide a one-line explanation before the relevant prompt. Do not describe speculative second-round prompts as visually informed improvements, because no rendered evidence exists. Put the selected prompts last, with nothing after the final prompt block.

## Adapt to another generator

When producing a version for another image generator, preserve the core concept, subject, mood, composition, palette, and format. Change only the syntax and controls required by the target tool.

Use compact prose for prose-oriented generators and subject-first descriptive phrases for phrase-oriented generators when appropriate. Verify current tool conventions before using model versions, flags, or proprietary controls. If a version choice materially affects results and cannot be verified, ask once rather than guessing. Keep variants separate and clearly labeled.

## Learn from completed work

After the user selects an image, accepts a prompt, or gives clear feedback, retain only durable, authorized lessons: recurring composition problems, missing prompt constraints, reliable medium descriptions, destination crop requirements, or verified generator behavior. Distinguish explicit user feedback from aesthetic judgment.

Do not save private article content, names, sensitive details, credentials, account information, or one-off subject matter as reusable guidance. Do not turn a single successful image into a universal style default. If no general lesson emerged, make no workflow change.

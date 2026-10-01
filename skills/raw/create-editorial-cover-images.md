---
name: create-editorial-cover-images
description: Create eight article-specific editorial cover-image options through a two-round process: five distinct concepts, visual review of rendered results, and three evidence-based improvements using a user-chosen image generator.
---

# Create editorial cover images

Turn an article into eight finished cover-image options. Develop five distinct concepts, generate and inspect every result, then create three improvements based on what actually worked. The user chooses from finished images that have a clear visual and emotional connection to the article.

Use the user’s chosen image generator, publishing destination, and delivery method. Do not assume a particular service, account, visual medium, palette, or aspect ratio. If the user explicitly asks for prompts only, use the prompt-only branch instead of generating images.

## Purpose, permissions, and scope

Use the complete article as the creative source. If the article is unpublished, private, or contains personal information, confirm that the user is authorized to use it for this purpose. Use only the minimum text and facts needed to create the visual brief. Do not send the whole article to an external generator unless that is necessary, authorized, and expected by the user.

Do not invent factual scenes, personal histories, locations, events, or identities that the article does not support. A cover image may be metaphorical, but it should not imply that a fictional visual is documentary evidence. Avoid unrelated sensitive details, recognizable private individuals, logos, or confidential material unless the user has clearly requested and authorized their use.

If the intended output involves a real person, make the representation appropriate to the article’s purpose and audience. Use an anonymous or non-identifying depiction when a specific identity is unnecessary.

## Establish the creative brief

Read the complete article before developing concepts. A title alone is rarely enough to distinguish an image that belongs to this piece from a generic illustration of its topic. If the copy is missing, ask for it before beginning.

Identify the following privately as working notes:

- The **central move**: the idea, realization, or change in perspective the reader should take away.
- The **emotional progression**: where the piece is quiet, tense, hopeful, reflective, challenging, or conclusive.
- The **concrete images, actions, and metaphors** already used in the writing. These often make stronger visual anchors than invented imagery.
- The **tone of voice**: for example, sober, playful, urgent, reflective, celebratory, or defiant.
- Any factual, ethical, or representational constraints that affect the image.

Use this analysis to make the concepts specific. Do not begin by giving the user a long article summary unless they ask for one.

Reuse preferences that the user has already supplied. Ask only for missing choices that would materially change the result. Ask related questions together and collect all outstanding answers before treating a partial reply as the full brief.

1. **Mood:** Offer three or four interpretations grounded in distinct beats of this article. Explain what each one emphasizes. For example, an article about recovering confidence might support a quiet rebuilding mood, a forward-motion mood, or a hard-won hopeful mood.
2. **Subject:** Offer suitable approaches such as a human figure, landscape only, a single symbolic object, an interior scene, or an abstract composition. Respect restrictions on people, settings, objects, or realism.
3. **Palette:** Offer a few palettes that support the article and the chosen mood. Describe contrast, value, and lightness as well as naming colors, so the choice remains clear for people who do not distinguish colors in the same way.
4. **Orientation:** Establish the final placement and crop. Common options include a wide header, square social preview, portrait cover, or a user-supplied size. Verify destination dimensions when possible rather than assuming that one publishing format fits all.
5. **Medium or style:** If the user has not already chosen it, establish whether the image should read as photography, painting, illustration, collage, printmaking, or another medium.

Keep a short working brief with the agreed mood, subject restrictions, palette, medium, format, intended destination, and generator. Carry it through both rounds. Do not repeatedly ask for the same preferences during iteration.

## Propose five distinct concepts

Present exactly five ideas in a numbered list. Each idea must include:

- A short title.
- A one- to three-sentence description of what the viewer sees.
- A brief statement of the article idea or emotional beat that the concept expresses.

The concepts must be meaningfully different. Vary subject, scale, composition, visual metaphor, and emotional emphasis. Five slight variations of one scene are not a useful range.

Unless the user’s restrictions rule them out, include at least:

- One landscape-only or environment-led concept.
- One single-object or symbolic concept.

Check that every concept earns its place by connecting to this specific article. Replace any concept whose explanation could fit almost any article on the same broad topic.

Give a one-line initial recommendation, then generate all five when the requested deliverable is finished images. Do not make the user choose a concept before the first round unless they specifically ask to do so. The point of the first round is to provide real visual alternatives for comparison.

## Write strong visual prompts

Write one self-contained prompt per concept. Use concrete visual direction without overloading the generator with competing instructions. Adapt the final syntax to the chosen generator, but build each prompt from this structure:

```text
Create one image: [medium, format, and overall editorial character].

Subject: [what is visible, its action, prominence, and position. Put relevant exclusions here, such as no visible face, no logos, or no lettering.]

Setting: [surroundings, depth, layers, and foreground-to-background relationships where useful.]

Light and palette: [time of day or light direction, specifically named colors, contrast, and transitions.]

Technique: [visible traits of the selected medium, edge quality, texture, detail level, and negative space.]

Mood: [the intended emotional effect and its connection to the article’s central move.]

Composition: [focal point, eye path, placement of major shapes, crop, dimensions, or aspect ratio.]

Avoid: [only artifacts, content, or visual conventions that conflict with the brief.]
```

Name colors and relationships rather than relying only on words such as “warm,” “moody,” or “dramatic.” For example, “pale ochre ground fading into blue-grey shadow, with a muted violet horizon” is more actionable than “warm evening light.” Name colors to improve precision, but also describe brightness, darkness, and contrast so the direction does not depend only on color labels.

Describe the physical behavior of the chosen medium. A watercolor image may need wet-on-wet washes, pigment blooms, transparent glazes, visible paper, selective edges, and unpainted space. A charcoal drawing may need broad tonal masses, broken edges, and paper grain. A photograph may need a lens perspective, depth of field, natural light direction, and believable material detail.

Put important exclusions near the instruction they constrain, not only at the end. For example, say “an anonymous figure seen from behind, with no facial detail” in the subject description. Use a final avoidance list as reinforcement, not as the only place where a critical constraint appears.

Unless requested, avoid unintended lettering, logos, borders, watermarks, and interface-like elements. If the cover needs space for later typography, specify the location and character of that negative space. Do not request text rendered inside the image unless the user has explicitly approved it.

Send the generator only the visual brief required to make the image. Do not paste the full article, private correspondence, or unrelated user data by default.

## Generate the first five

Use the chosen generator’s supported workflow. Explicitly request an image so a text response is not mistaken for the deliverable. Respect access controls, spending limits, account boundaries, content policies, and live approval decisions. If the service is unavailable, report the blocker and ask before moving article material to a different service.

Maintain a working record for every option:

| Option | Record to keep |
|---|---|
| 1–8 | Title, concept, submitted prompt, generation status, output location, and visual-review notes. |

Preserve the full submitted prompt so a cut-off or failed request can be repaired accurately. Start independent jobs concurrently only if the tool safely supports it. Keep browser or interface actions sequential when they share focus or state.

For each option, verify all of the following:

1. The generator received the intended complete prompt.
2. The request became an image-generation task rather than a text-only response.
3. A real image completed and can be opened at a useful size.
4. The output location or link is real and observed, not inferred or invented.

An accepted submission, elapsed time, loading placeholder, thumbnail shell, progress indicator, or textual description is not proof of image completion. If an error appears, first check whether an image already exists before retrying, to avoid unnecessary duplicates. Keep unsuccessful attempts separate from finished options.

## Inspect all five before creating improvements

View every first-round image at a useful size. Evaluate the actual pixels, not the generator’s description and not what the prompt was meant to produce. Also inspect each result as a small preview, because a cover image must still communicate when reduced or cropped.

For each image, record:

- Whether it communicates the article’s central idea and emotional tone.
- Whether the subject or visual action reads quickly, with a clear focal point.
- Whether the requested style, palette, orientation, and composition survived generation.
- Whether it feels too busy, generic, sentimental, static, literal, or visually confusing.
- Any visible anatomy, object, perspective, texture, construction, lettering, or watermark-like artifacts.

Only after reviewing all five should you design the next three prompts. Tie every improvement to visible evidence: identify the strength to retain, the weakness to correct, and the visual change most likely to help. Do not prewrite the second round before seeing the first results.

A useful second-round spread is often:

1. A refinement of the strongest first-round image.
2. A concept combining strengths observed in two different images.
3. A new direction that fills a missing emotional or compositional gap.

Use judgment instead of forcing this pattern. The important requirement is that options six through eight are informed by inspection and add meaningful alternatives.

Fix causes rather than decorating symptoms. If an image is cluttered, reduce objects and competing focal points before adding detail. If a painting looks like a photograph with a style filter, request fewer large shapes, selective edges, and the actual marks of the chosen medium. If a scene resembles generic travel, workplace, or lifestyle imagery, reconsider the action or metaphor rather than adding ornamental detail.

Give the user a short progress update: state what the first round revealed and what the next three images will improve. Continue without asking for another selection unless the user has asked to approve each stage.

## Generate, inspect, and deliver options six through eight

Generate three new images from the revised prompts. Keep the first five available so the user can compare original directions with improvements. Inspect each new output using the same completion checks and visual criteria.

If a generation fails or returns text only, repair it where possible in the same task context. Do not count an unsuccessful attempt as a finished option. Do not silently replace a missing image with an old result, a written prompt, or a different concept.

Before delivery, verify that there are eight distinct completed outputs that you personally inspected. Check that their numbering and titles match the working record, and that each output can be accessed from the handoff method supported by the chosen generator.

Give a short recommendation naming the strongest rendered option and why it fits the article. Then provide a numbered list of all eight titles and verified output locations, clearly marking options six through eight as the second round. Keep this list as the final deliverable block.

If rate limits, access requirements, or repeated errors prevent completion, state exactly which options are finished, which are blocked, and what action is needed to resume. Preserve useful work. Never claim that eight completed images exist when some are only prompts or unsuccessful attempts.

## Prompt-only branch

When the user explicitly requests prompts only, do not generate images. Read the article, collect or reuse the same creative preferences, and propose five concepts. Wait for the user to select concepts unless they have already selected them or asked for all five prompts.

Write each selected prompt in its own fenced code block using the prompt structure above. If combining concepts, give one short line explaining the combination before the prompt. Keep the selected prompts last, with nothing after the final prompt block.

Do not describe hypothetical second-round prompts as if they were informed by visual review. Without rendered images, there is no evidence base for that stage.

## Adapt to another generator

When the user asks for a version of the same concept in another image generator, preserve the concept, mood, composition, palette, and format. Change the prompt structure only where the target tool requires different conventions.

A prose-oriented generator may work best with a compact paragraph. A parameter-oriented generator may work better with short descriptive phrases plus verified controls for aspect ratio, style, or quality. Check current supported conventions before specifying flags, model versions, or unsupported controls. If a version materially affects the prompt and remains unclear, ask once rather than guessing.

Keep platform variants separate and clearly labeled. Changing tools should not quietly change the underlying creative idea.

## Learn from completed work

After the user chooses an image, accepts a prompt, or provides clear feedback, identify reusable lessons only when the user has authorized memory or workflow updates. Favor general lessons about article interpretation, palette specificity, composition, medium constraints, or generator behavior.

Distinguish explicit user feedback from your own aesthetic judgment. Do not make one article’s subject, one person’s preferred style, or a one-off generation result into a universal default. Keep private article content and personal details out of reusable notes. If there is no durable lesson, make no update.

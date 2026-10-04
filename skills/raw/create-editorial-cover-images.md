---
name: create-editorial-cover-images
description: Create editorial cover images from an article through five distinct concepts, visual review, and three informed improvements using the user’s chosen image-generation workflow. The method produces eight completed options or, when requested,.
---

# Create editorial cover images

Turn an article into eight finished cover-image options. Develop five distinct concepts, generate and inspect every result, then create three improvements based on what actually worked. The user chooses from finished images that clearly connect to the article.

Use the user’s chosen image generator and publishing format. Do not assume a particular account, service, medium, palette, or publication platform. If the user explicitly requests prompts only, follow the prompt-only branch instead of generating images.

When working with unpublished drafts, private communications, or records about people, have a legitimate editorial purpose and clear authorization. Use only the minimum relevant material needed to understand the article. Do not include unrelated personal details, identifiable information, or confidential facts in prompts unless the user has specifically authorized their use and the intended output boundary makes that appropriate.

## Establish the brief

Read the complete article before developing concepts. A title alone is rarely enough to distinguish an image that belongs to this piece from a generic illustration of its topic. If the copy is missing, ask for it before generating.

Identify the article’s central move: the idea, realization, or changed perspective a reader should take away. Notice its emotional progression, including where it becomes quieter, turns, or reaches its conclusion. Extract concrete images, actions, and metaphors already present in the writing. Note the tone, such as reflective, urgent, hopeful, sober, or celebratory, because it constrains the image’s mood.

Use this analysis to make the creative work sharper. Do not begin with a long summary unless the user asks for one. Never invent factual events, places, people, or claims that the article does not support. A visual metaphor may interpret the article, but it should not imply that an imagined scene is a literal depiction of real events.

Reuse preferences already supplied. Ask only for missing choices that materially change the result, keeping related questions together. Collect all outstanding answers before treating a partial reply as the complete brief.

Ask about the following areas when they are not already clear:

- **Mood:** Offer three or four interpretations grounded in particular beats of this article. Explain what each option emphasizes, so the user chooses among real readings of the piece rather than generic adjectives.
- **Subject:** Explore appropriate options such as an anonymous human figure, a landscape, a single symbolic object, or an abstract composition. Respect restrictions on people, places, representations, or factual depictions.
- **Palette:** Offer several palettes suited to the selected mood. Name colors specifically and describe contrast, value, and lightness as well, so the decision does not depend on color labels alone.
- **Orientation:** Establish where the image will appear and how it will be cropped. A wide header, square preview, portrait cover, and social card need different compositions. Use dimensions supplied by the user or verified for the destination.
- **Medium or style:** Establish whether the image should be photographic, painted, drawn, collaged, graphic, or another medium. If the user names a style up front, treat that as the default rather than asking again.

A useful question format is:

1. **Mood:** Which emotional entry point should lead: [article-specific interpretation A], [article-specific interpretation B], or [article-specific interpretation C]?
2. **Subject:** Should the image center on [an article-specific figure or action], a landscape, a symbolic object, or an abstract treatment?
3. **Palette:** Which palette best supports that reading: [specific palette A], [specific palette B], or [specific palette C]?
4. **Format:** Is this for a wide header, a square preview, a portrait cover, or another specified placement?

Keep a concise working brief containing the agreed mood, subject restrictions, palette, medium, format, generator, and any accessibility or brand constraints. Carry it through both rounds without asking the same questions again.

## Propose five distinct concepts

Present exactly five ideas in a numbered list. Each idea needs:

- A short title.
- A one- to three-sentence description of what the viewer sees.
- A brief statement of the article’s idea or emotional beat that the concept expresses.

Vary the subjects, compositions, and interpretations. Five minor changes to one scene do not provide meaningful range. Unless subject restrictions rule them out, include at least one landscape-only option and one single-object or symbolic option. An anonymous, back-turned, or distant figure can be useful when a human presence is needed without making the image about a specific person, but it is not a required default.

Check that every concept has a specific reason to belong to this article. Replace any concept whose explanation could accompany nearly any article on the same broad topic.

Give a one-line initial recommendation, then generate all five without asking the user to choose first. The first round provides visual material for comparison. Do not stop at concepts or written prompts when finished images were requested.

## Write useful visual prompts

Write one self-contained prompt per concept. Keep visual direction specific enough to render while avoiding competing instructions. Use this structure, combining sections where that reduces repetition:

```text
Create one image: [medium, format, and overall visual character].

Subject: [what is visible, its action, prominence, and position; place relevant exclusions alongside the description].

Setting: [surroundings, depth, and foreground or background relationships where useful].

Light and palette: [direction and quality of light, specific colors, contrast, and transitions].

Technique: [visible properties of the chosen medium, edge treatment, texture, detail level, and negative space].

Mood: [the intended feeling and its connection to the article’s central idea].

Composition: [focal point, where the eye enters, placement of major shapes, requested dimensions or aspect ratio, and crop considerations].

Avoid: [only the artifacts, visual conventions, or content that conflict with this brief].
```

Name colors and their relationships instead of relying only on words such as *warm* or *moody*. For example, “pale ochre field against deep violet shadows, with cool blue-grey at the horizon” makes a more usable visual decision than “dramatic warm lighting.” Name colors to clarify the selected palette, not to impose a fixed aesthetic on every article.

Explain the physical appearance of the chosen medium. A watercolor image may need broad wet-on-wet washes, visible pigment bleeds, textured paper, selective edges, transparent layers, and substantial unpainted space. A charcoal drawing may depend on broad tonal masses, broken edges, and visible paper. A photograph may depend on lens perspective, depth of field, natural light, and believable material detail. Do not combine incompatible technique instructions merely because they appeared in another prompt.

Place exclusions beside the relevant positive instruction as well as in a final list when helpful. For example, say “distant silhouette with no facial detail” in the subject description rather than relying only on “no faces” at the end. If empty space is needed for later typography, specify where it belongs. Establish whether lettering is desired; otherwise prevent unintended text, logos, borders, and watermark-like artifacts.

Send the generator only the visual brief needed to create the image. Do not paste a full unpublished article, private records, or unrelated personal context by default. Use article-specific facts only when supported by the copy, authorized, and appropriate for the intended publication.

## Generate the first five

Use the chosen generator’s supported workflow. Explicitly request an image so a text response is not mistaken for the deliverable. Respect existing access, spending, licensing, approval, and account boundaries. Do not bypass approval gates, inspect unrelated account areas, or move content to another service without the user’s agreement.

If the selected service is unavailable, report the limitation and attempt safe recovery within the authorized workflow. If a replacement generator would require sending material to a different service, ask before doing so.

Keep a working record for each option: number, title, concept, submitted prompt, generation status, output location, and review notes. Preserve the complete prompt so a truncated or failed submission can be repaired accurately. Start independent jobs concurrently only when the tool supports that safely and within its limits.

Confirm each submission was accepted with the intended brief. Then confirm that the actual image completed and can be opened at a useful size. An accepted request, elapsed time, placeholder, progress indicator, thumbnail, or text description does not establish completion. If an error appears, check whether an image already exists before retrying to avoid duplicate work. Keep failed attempts separate from completed options.

## Inspect all five before improving

View every completed image at a useful size and evaluate the actual pixels. Do not judge only the generator’s description or what the prompt intended. Also inspect a small preview, because a cover must communicate when reduced or cropped.

For each image, record:

- Whether it communicates the article’s central idea and emotional tone.
- Whether the subject and action read immediately, with a clear focal point.
- Whether the requested style, palette, orientation, and composition survived generation.
- Whether it feels too busy, generic, sentimental, static, or overly literal.
- Any visible anatomy, object, perspective, construction, or lettering artifacts.

Only after reviewing all five, design three new prompts. Tie each improvement to a visible observation: a strength to retain, a weakness to correct, and a change likely to help. Do not prewrite this round before seeing the first outputs.

A useful spread is one refinement of the strongest image, one combination of strengths from different images, and one new concept addressing a gap. Use judgment when another distribution would better serve the article. Each new image must contribute a meaningful alternative rather than a near-copy of an earlier result.

Fix the cause of a weak result. If a composition is cluttered, reduce the number of objects or competing focal points before adding more instructions. If an image looks like a photograph with a paint filter, request fewer large shapes, selective edges, genuine medium marks, and more negative space. If a scene resembles generic travel, workplace, or lifestyle imagery, reconsider the action or metaphor before adding decoration.

Give a short progress update explaining what the first images revealed and what the next three will improve. Continue without requesting another selection or repeating the creative brief.

## Generate, review, and deliver options six through eight

Generate three new images from the revised prompts. Keep the first five intact so the user can compare originals with improvements. Inspect each new result using the same visual criteria and completion checks. Repair failed generation attempts where possible without counting them as finished options or substituting an old image.

Before delivery, verify that there are eight distinct completed outputs that you personally inspected. Check that each can be opened from the final handoff and that titles and numbering match the working record. Use accessible files, saved outputs, or verified links supported by the chosen generator. Preserve the finished outputs for the user to compare.

Recommend the strongest rendered image in a short sentence explaining why it fits the article. Follow with a numbered list of all eight titles and their outputs, clearly identifying the final three as the second round. Keep the outputs as the final deliverable block. Avoid turning the handoff into a long design report.

If access, rate limits, policy restrictions, licensing concerns, or repeated generation errors prevent completion, state exactly which options are finished and which remain blocked. Preserve useful work for resuming. Do not claim eight images exist when some are only prompts, placeholders, or unsuccessful attempts.

After completion or selection, learn only from explicit user feedback and clearly observed results. When the user has authorized memory or workflow updates, save reusable lessons about article interpretation, composition, prompt constraints, or verified generator conventions. Keep private article content out of reusable lessons. Do not convert one article’s subject or a single successful image into a permanent universal default.

## Prompt-only branch

When the user explicitly wants prompts only, do not generate images. Read the article and reuse or collect the same creative preferences. Propose five concepts, then wait for a selection unless the request already specifies concepts or asks for all prompts.

Write each selected prompt in a separate fenced code block using the prompt structure above. If combining concepts, give a one-line explanation of the combination before the prompt. Do not describe hypothetical second-round prompts as improvements informed by visual review, because no rendered results have been inspected. Put the selected prompts last, with nothing after the final block.

## Adapt to another generator

When the user requests a version for another generator, preserve the concept, mood, composition, palette, and format. Change prompt structure or parameters only as needed by the target tool. A prose-oriented generator may suit a compact paragraph, while another may work better with front-loaded descriptive phrases and separate controls.

Check the target tool’s supported conventions before specifying parameter flags, model versions, aspect-ratio syntax, seed controls, or style settings. If a version matters and remains unclear, ask once rather than guessing. Keep each platform variant separate and clearly labeled. Changing generators should not quietly change the underlying image idea.

---
name: cover-images
description: Creates editorial cover images for articles: five distinct concepts, a close review, then three improved versions. Use when someone needs a post header, article cover, or image prompt.
---

# Create editorial cover images

Turn a written article into eight finished editorial cover-image options: five genuinely different first-round concepts, a close look at every rendered result, then three new options based on what the first round actually revealed. The user should receive finished images that clearly relate to the article, not just a list of hypothetical prompts.

## Quick version

- Paste the full article into your assistant. Ask it to identify the central move, the emotional beats, any concrete images or metaphors the article already uses, and the tone. These shape every later choice.
- Settle four preferences with options written for this article: mood, subject, palette, and orientation. Also pick a medium if you have not already.
- Ask for exactly five distinct concepts. Each needs a title, a one- to three-sentence description of what the viewer sees, and the article beat it expresses. Include at least one landscape-only and one symbolic-object idea.
- Turn each concept into a structured prompt with precisely named colors and exclusions placed next to the instructions they qualify. Generate one image per prompt in your image tool.
- Look at all five at full size and at thumbnail size. Note what works and what fails. Only then write three improved prompts, each tied to a specific observation.
- Keep all eight images, compare them side by side, and choose.

## 1. Check readiness

A cover image should do more than decorate a topic. It should express the article's central move, emotional register, or defining metaphor in a form that still reads at thumbnail size.

Before generating, confirm:

- You have the complete article. Do not create article-specific concepts from a title alone; they come out generic. If only a summary is available, say the images will be based on the summary.
- The image generator, publication destination, and approved access method are clear. Do not assume a particular service, account, house style, or aspect ratio. If the chosen service is unavailable, report the blocker and ask before moving article material to a different service.
- The intended placement, crop, and output format are known or can be chosen with the user.
- Restrictions about people, places, brands, factual depiction, lettering, or sensitive content are known.

Do not paste a full unpublished article into an image generator. Extract only the visual facts, metaphors, and tone the prompt needs. Do not imply that an imagined scene documents a real event unless the article supports that and the user wants a factual depiction.

If the user explicitly asks for prompts only, follow section 8.

## 2. Read the article and build the brief

Read the article end to end before proposing anything. Identify internally:

- **Central move:** the idea, tension, or change in perspective the reader should retain.
- **Emotional progression:** where the writing is quiet, where it turns, where it lands.
- **Concrete source imagery:** objects, places, actions, and metaphors already in the text. These are strong candidates because they visualize what the article already says.
- **Tone:** reflective, investigative, urgent, hopeful, defiant, celebratory, or sober.
- **Editorial constraints:** what must not be shown and what a literal depiction could get wrong.

Use this analysis to sharpen decisions; do not return a long summary. Never invent facts about the article. If the user mentions a name or place, use it only if it actually appears in the source.

Reuse preferences already given in the conversation. Ask only for missing choices that materially change the output, and collect all outstanding answers before treating a partial reply as the whole brief. Write options that refer to specific beats of this article, so the user picks between real interpretations rather than abstract preferences.

1. **Mood:** three or four legitimate readings of this article, each naming the beat it leads with.
2. **Subject:** for example an anonymous figure seen from behind, landscape only, a single symbolic object, or an abstract composition. Anonymous figures read as universal, but a landscape or one object is often more elegant.
3. **Palette:** three or four palettes with named colors, value range, and contrast. Do not rely on telling two colors apart (such as red versus green) as the only difference between options.
4. **Orientation:** wide header, square preview, portrait, or a custom ratio. Verify the destination's requirements rather than carrying dimensions over from another publication, and mark the destination's native shape as recommended.

If the medium is still open, choose it for the article and audience. A reasonable adjustable default is loose, hand-made editorial illustration (watercolor or ink) with plenty of empty space and no text, borders, or watermarks. If the user signals another style, such as a photograph, follow it.

Keep a compact working brief: central move, mood, subject constraints, palette, medium, orientation, generator, and exclusions. Carry it through both rounds without asking again.

## 3. Develop five distinct concepts

Present exactly five concepts, each with a short title, a one- to three-sentence description of what the viewer sees, and a half-line on the beat it expresses. If you cannot name the beat, cut the concept.

The five must differ in subject, composition, metaphor, and emotional emphasis. Five variations of one person in one setting is a fail. Unless the brief rules them out, include a landscape-only concept and a single-object concept.

Test each concept: could the same explanation fit almost any article on this topic? If yes, replace it with something tied to this article's argument, image, or turn.

Give a one-line recommendation, then generate all five without asking the user to pick first. The rendered images are what they choose from.

**Invented example.** For a fictional essay in *The Lantern Quarterly* about a retired lighthouse keeper learning to sleep through the night:

1. **Dark tower** (landscape): an unlit lighthouse against a pale dawn sea. *Beat: the relief of no longer keeping watch.*
2. **The cold lamp** (object): one brass lamp resting on a windowsill. *Beat: a tool set down.*
3. **Turned away** (figure): a back-turned figure walking inland, the tower small behind. *Beat: choosing a new direction.*
4. **Tide clock** (abstract): concentric washes like a slowing beam. *Beat: time loosening its grip.*
5. **Open shutters** (interior): morning light across an unmade bed. *Beat: the first full night's sleep.*

## 4. Write effective visual prompts

Write one self-contained prompt per concept and ask explicitly for an image, so the generator does not return text or another prompt.

```text
Create one image: [medium, overall editorial character, and requested format].

Subject: [what is in frame, where, what it is doing, scale and prominence. Put relevant exclusions here, such as no recognizable face, no logos, no text.]

Setting: [surroundings, depth, foreground and background, what recedes or stays empty.]

Light and palette: [specific colors, transitions, light direction, contrast, atmosphere.]

Technique: [physical properties of the medium, texture, edge treatment, level of detail, negative space, and what to avoid such as digital sheen.]

Mood: [the feeling, anchored to the article's central move.]

Composition: [focal point, eye path, horizon placement, crop, negative space, aspect ratio.]

Avoid: [artifacts, conventions, or content that conflict with the brief.]
```

**Naming colors precisely matters more than any other single choice.** "Pale ochre ground, slate-blue shadows, faded apricot light, a deep violet horizon" beats "warm and moody." Say how colors relate, where transitions happen, and how saturated they are.

Describe the medium's actual properties. For watercolor: broad wet-on-wet washes, pigment blooms, visible paper grain, transparent layers, selective edges, unpainted paper. For photography: lighting, distance, depth cues, and realism level.

Put important exclusions inside the positive description as well as in the final line. "A back-turned silhouette with no visible facial features" lands harder than a separate "no faces" list.

## 5. Generate the first five

Use the chosen generator through an authorized method. Respect spending limits and approval gates, and never bypass a login, approval request, rate limit, or access restriction. If blocked, state what is blocked, preserve completed work, and ask only for the action needed to resume.

Keep a working record:

| # | Title | Prompt | Status | Output location | Review notes |
|---|---|---|---|---|---|
| [1] | [Dark tower] | [full submitted prompt] | [generating / done / failed] | [verified link or file] | [observations] |

For each option, use a separate generation context, enter the complete prompt, check the visible input contains all of it, send, and confirm a rendered image exists. A spinner, placeholder, elapsed time, or the model's description is not proof of completion. If an error appears, check whether an image already finished before retrying, to avoid duplicates. Keep failed attempts separate from finished options.

Independent jobs can run at the same time when the tool supports it, but keep interactions with one shared interface sequential.

## 6. Inspect all five before improving

View every image at useful size and at approximate thumbnail size. Judge the pixels, not the prompt or the generator's claims. For each, ask:

- Does it communicate the central idea and tone?
- Is the focal subject or action immediately clear?
- Did the medium, palette, shape, and composition survive?
- Is it too busy, generic, sentimental, static, or literal?
- Are there anatomy, perspective, object, lettering, or other artifacts?
- Does it still work when cropped or reduced?

Only after reviewing all five, write prompts six through eight. Do not prewrite them. For each, record the strength to keep, the weakness to fix, and the visible change expected. A useful spread is one refinement of the strongest image, one combination of strengths from different images, and one new direction that fills a gap. Use judgment rather than forcing that pattern.

Fix causes, not symptoms:

- Cluttered scene: remove competing objects or simplify the action before adding detail.
- Looks like a photo with a painted filter: ask for fewer large shapes, selective edges, real negative space, and the medium's actual marks. Piling on concrete detail can overpower requests to simplify.
- Feels like generic stock, travel, or office imagery: rethink the metaphor or viewpoint instead of adding props.

Give the user a short progress note on what the images revealed and what the next three will improve, then continue without asking for a selection.

## 7. Generate options six through eight and hand off

Generate the three new images in fresh contexts, leaving the first five unchanged for comparison. Apply the same submission, completion, and inspection checks. If one fails or returns only text, repair it in the same context. Never count a failed request as finished or silently substitute an older image. If a limit or gate stops you, say exactly which options are complete and which are blocked.

Readiness gate before delivery:

- Eight distinct completed images, not prompts or placeholders.
- Each inspected at useful size.
- Each opens from its final location within the user's access boundary.
- Titles, numbers, and locations match the record.
- Options six through eight are marked as second round.

Give a one-sentence recommendation based on the rendered results, then a numbered list of all eight titles and verified locations, marking the second round. Make that list the final block. Keep any explanation of unusual interpretations brief rather than writing a design report. Download or export the chosen image only when asked or needed next.

## 8. Prompt-only branch

When the user explicitly wants prompts only, do not generate images. Read the article, settle the preferences, and propose five concepts. Wait for a selection unless the user already chose or asked for all prompts.

Deliver each selected prompt in its own fenced code block using the structure above, with readable section breaks. If combining concepts, add one sentence explaining the combination before that prompt. Do not invent a "visually informed" second round when nothing was generated. Put the prompts last, with nothing after the final block.

## 9. Adapt to another generator

Preserve the subject, composition, palette, mood, exclusions, and format; change only syntax and controls. Some tools prefer comma-separated phrases with the subject first and trailing parameters for ratio and style; others prefer a tightened prose paragraph. Check current conventions before using parameter flags or model versions, and if a version matters and is unclear, ask once rather than guess. Keep variants separate and labeled. A new tool should not quietly become a new concept.

## Optional extras

### Working through a connected browser or agent

- Open a new conversation or tab per option and do not take over the user's existing conversations.
- Many chat-based generators handle a single paragraph more reliably. Flatten the finished prompt into one line and start it with an instruction to create one image now.
- Inspect the live input before typing, read the text back after entering it, and locate the current send control rather than relying on a remembered label. If the prompt was cut off, stop and resend the full brief in the same conversation.
- Record each conversation's observed address; never construct one. Check for loaded image elements, since interface labels change.
- Scroll with the tool's supported controls rather than scripts that modify the page.
- If your agent tool closes tabs it created at the end of a turn, mark all eight finished tabs to stay open, and re-mark them on later turns. Keep a separate "needs user input" handoff only for genuinely unfinished pages.

### Designing a family of small icons

The same concept-review-improve loop works for app or bot icons:

- Study existing icons in the family first and keep the shared style: for example flat shapes, a fixed two- or three-color palette on a plain background, no text, outlines, gradients, or shadows. Each new icon should be distinctive and about its own app, not a variation of a sibling.
- Free or limited generator plans may cap daily images, so budget generations.
- Treat generated images as concepts. Redraw the chosen one as vector art, render it to a large square image, and build a comparison sheet showing each option at large, medium, and tiny sizes (for example 240, 64, and 32 pixels; adjust to the platform).
- Draw each single-color region as one path. Adjacent same-color shapes can leave faint anti-aliasing seams.
- Upload through the platform's settings, reload to confirm it saved, and store the final file alongside the project.

### Icons that share one brand mark

Workspace, community, or team icons often follow a different rule from app icons: every variant uses the same official mark, and only the setting changes.

- Take the mark from the organization's official source file and keep it exact. Do not redraw, restyle, or generate a new symbol.
- Make each variant distinct through a background tied to that group or place, such as a texture, material, or landscape that people there will recognize.
- *Invented example:* the fictional Harbor Lane Collective puts its white mark on a deep teal wave texture for its waterfront studio, and on pale sandstone for its desert field office.
- Some upload tools can only read files inside the agent's own working area. Copy the final image there first, follow the platform's upload and crop steps, reload to confirm the change, and keep an archive copy in the user's chosen folder.

### Learn from outcomes

After the user chooses, accepts a prompt, or stops iterating, capture durable lessons only. Strong signals: they rejected your recommendation (diagnose whether the read, composition, mood, or generation failed), they rewrote part of a prompt (update the template), they asked for color specifics you missed, or an image failed in a way the prompt should have prevented. Separate their feedback from your own taste, keep lessons general rather than tied to one article, and make no change after a clean run.

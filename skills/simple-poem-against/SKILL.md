---
name: simple-poem-against
description: Create atmospheric Chinese poetry zine posters that first judge the source mood, then preserve its feeling, add a reflective turn, or challenge it with restrained satire as appropriate. Integrate source text, optional secondary text, imagery, typography, adaptive aspect ratios, and physical material effects. Use for poems, quotations, prose fragments, screenshots, photos, themes, or moods when the user wants concept exploration, direct generation, multiple-source batches, or revision of image-led and type-led bitmap posters.
---

# Simple Poem Against

Create poetry posters in which source text, optional secondary text, imagery, typography, canvas shape, and printed paper behave as one composition.

Use the built-in image-generation capability. Do not generate images while the user explicitly wants discussion only.

## Load References

Read only the references required for the task:

- Read [source-intake.md](references/source-intake.md) for screenshots, scans, photos containing text, uncertain attribution, or multiple sources.
- Read [countertext.md](references/countertext.md) whenever deciding whether secondary text is needed or writing it.
- Read [material-grammar.md](references/material-grammar.md) before choosing imagery, composition, paper behavior, or color.
- Read [quality-gate.md](references/quality-gate.md) before generation and delivery.

## Choose an Execution Mode

Determine the mode and requested image count before concept work.

### Explore

Use when the user asks for options, wants to compare directions, or gives an ambiguous source.

1. Propose 2 concepts for a short quotation and 3-4 for a longer or visually ambiguous poem.
2. Stop for selection.
3. After selection, generate the requested count; default to image-led plus type-led.

### Direct

Use when the user says `直接生成`, `你决定`, `自由决策`, `先来一张`, or otherwise asks to skip selection.

1. Develop candidates internally.
2. Choose the strongest concept.
3. Generate exactly the requested count without exposing concept cards first.

### Batch

Use for multiple poems, quotations, or images.

1. Keep source, title, attribution, countertext, and filename isolated for each item.
2. Infer count conservatively: two sources plus `再来两张` normally means one per source.
3. Never multiply the requested count merely because two variants are the default in Explore mode.

### Revision

Use when the user critiques or selects an existing poster.

1. Preserve approved text, metaphor, color, and composition unless the critique targets them.
2. Change only the specified defect.
3. Generate only the requested replacement variants.

## Interpret the Source

Extract:

- the exact title, work title, author, and strongest source line;
- the dominant emotion, emotional temperature, and movement;
- whether the source is sincere, playful, tender, reflective, absolute, self-deceiving, or institutionally absurd;
- the suitable relation mode: **Preserve**, **Resonance**, **Tension**, or **Satire**;
- what the source asks the reader to believe, only when considering Tension or Satire;
- one defensible target, contradiction, or consequence, only when considering Tension or Satire;
- concrete images already present;
- one physically imageable emotional fact, relation, contradiction, or consequence.

Choose the relation mode before writing any secondary text:

- **Preserve:** keep sincere happiness, lightness, tenderness, wonder, or calm intact. Do not add cynicism merely because the skill name contains `against`.
- **Resonance:** add a companion line only when it deepens atmosphere without correcting or mocking the source.
- **Tension:** use for philosophical, universal, or absolute claims that benefit from a question, boundary, cost, or consequence.
- **Satire:** reserve for visible self-deception, hypocrisy, convenient romance, institutional absurdity, or hidden cost.

When in doubt between Preserve and a more adversarial mode, choose Preserve. An omitted secondary line is a complete editorial decision, not a missing layer.

Preserve strong source objects such as a lake, key, window, leaf, classroom, moon, road, sea, or rain. Do not replace them with generic symbols.

Choose one coherent metaphor or one closely related pair. Do not illustrate every line.

## Build the Text System

Use up to four layers:

1. **Title:** exact and readable; wrap an explicitly supplied Chinese title in `《》`.
2. **Source quote:** one earned line representing the source claim.
3. **Secondary text:** optional; none in Preserve by default, companion text in Resonance, reflective counterpoint in Tension, or restrained countertext in Satire.
4. **Image-text:** optional 2-6 character fragments that behave as part of the scene or material.

Do not force every layer into every poster.

Keep title, quote, secondary text, and attribution fully readable. Allow only image-text to trade limited clarity for reflection, erosion, blur, cropping, or overlap.

Never create fake metadata, decorative English, dates, issue numbers, signatures, account names, pseudo-Chinese, or meaningless microtext.

## Concept Cards

In Explore mode, make concepts materially different in metaphor, relation mode, object set, composition, canvas, paper tone, accent, and emotional temperature.

Use this compact format:

```markdown
### 方向 N｜[name]

- 意象：
- 原文：
- 关系模式：
- 辅助文案：无 / 共鸣句 / 哲思转折 / 讽刺反文案
- 意象文字：
- 材质作用：
- 画幅与选择理由：
- 排版与第一视觉：
- 色彩锚点：
- 氛围：
```

Ask the user to choose, combine, or revise. Do not generate in the same turn unless the user explicitly requests immediate generation.

## Visual Contract

Obey a user-specified format. Otherwise choose the canvas from the source and composition:

- **3:5 vertical:** long vertical movement, descent, rain, road, solitude, time, or text-led breathing room.
- **4:5 vertical:** balanced image-text work, warm scenes, portraits, short quotations, and the safest general default.
- **1:1 square:** one short line, one centered object, specimen-like stillness, or icon-like conceptual compression.
- **4:3 horizontal:** dialogue, companionship, landscape, opposing objects, domestic happiness, or lateral narrative movement.

Use 4:5 when evidence is mixed. Keep paired image-led and type-led variants in the same aspect ratio unless the user is explicitly comparing canvases. Read [material-grammar.md](references/material-grammar.md) for selection and layout rules.

Keep:

- paper visibly material rather than a neutral background;
- serif, Song-style, typewriter, or monospaced typography;
- xerox, risograph, halftone, scan noise, ink bleed, torn fiber, abrasion, or controlled misregistration;
- one meaningful saturated accent, usually about 1%-4% of the canvas;
- quiet independent-zine or poetry-book sensibility.

Do not force warm beige paper. Choose paper tone, accent, and composition from the source and recent-output diversity check.

Avoid commercial film posters, glossy advertising, generic quotation cards, dense scrapbook decoration, neon, anime, and full-frame cinematic photography that hides the paper.

## Variant A — Image-led

Make imagery the first read at thumbnail size.

- Let imagery occupy roughly 35%-55% of the canvas.
- Keep roughly 40%-60% quiet field.
- Embed one or two image-text fragments into a named host surface such as water, fogged glass, road, wall, shadow, reflection, fabric, or torn print.
- Match the host surface's perspective, direction, focus, and material behavior.
- Let source or countertext interrupt, reveal, overwrite, or redirect the image.

Do not produce a photograph with a title above and a detached caption below.

## Variant B — Type-led

Make the quote-countertext collision the first read.

- Let typography occupy roughly 45%-70% of the canvas.
- Do not require a separate photograph.
- Let weather or material act on the substrate and one or two selected words.
- Use contrasts such as wet/dry, sharp/bleeding, fixed/drifting, printed/erased, or object/reflection.
- If a photo fragment appears, make it evidence or residue rather than a token thumbnail.

For classical Chinese verse or an explicitly requested ancient, quiet, or restrained mood, preserve the source quote's typographic dignity: use level baselines, coherent Song-style structure, and equal optical sizing across parallel lines by default. Express ascent, victory, freedom, or force through paper, image, spacing, color, or surrounding material—not by automatically tilting the quote, enlarging one character, or creating a staircase baseline.

Do not paste the same weather effect onto every character.

## Compile the Generation Prompt

Write four compact, renderable paragraphs:

1. **Canvas:** format, paper tone, density, first-read hierarchy, cluster size, and placement.
2. **Metaphor:** subjects, physical relation, composition family, material process, and coherence.
3. **Exact text:** list every rendered line separately; include title, selected quote, optional secondary text, image-text, and attribution decisions. State the host surface or targeted words.
4. **Color and avoids:** accent hue and share, print process, emotional temperature, recent-output differences, and hard exclusions.

State `render only these exact words; no other text`.

For image-led work, name the host surface and treatment for each image-text fragment. For type-led work, name the exact one or two words affected by material action. Never request a vague `artistic text effect`.

## Generate and Inspect

1. Lock mode, count, source, relation mode, aspect ratio, metaphor, source quote, optional secondary text, optional image-text, material action, composition, paper tone, accent, and mood.
2. Run the preflight in [quality-gate.md](references/quality-gate.md).
3. Issue one built-in image-generation call per distinct final asset.
4. Inspect at thumbnail and full size.
5. Apply the P0/P1/P2 rules from the quality gate.
6. Regenerate a failed variant once with a single targeted change and locked invariants.
7. If essential Chinese remains wrong, change strategy instead of repeating the same prompt.

## Deliver

Return:

- every requested image;
- the absolute saved path for every final asset;
- selected metaphor, relation mode, execution mode, and aspect ratio;
- exact source quote, optional secondary text, and image-text used;
- one short sentence explaining why the poster preserves, reflects on, or challenges the source mood.

Include full generation prompts when the user asks, when troubleshooting, or when prompt reuse matters. Otherwise return a concise prompt lock rather than repeating long prompts.

Do not overwrite existing assets. Follow the active project save-path instructions and keep the original generated file unless the user explicitly requests deletion.

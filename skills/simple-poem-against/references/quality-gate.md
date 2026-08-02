# Quality Gate

Use this reference before every generation call and before delivering final images.

## Text budget and locking

Treat these as soft reliability budgets:

- title: up to 14 Chinese characters;
- selected source quote: up to 28 Chinese characters;
- optional secondary text: up to 24 Chinese characters total;
- image-text: one or two fragments, each 2-6 characters;
- attribution: up to 6 Chinese characters.

When text exceeds the budget, select a stronger excerpt or ask whether exact long-form copy is essential.

List every rendered line separately in the prompt. Quote exact text and state `render only these words; no other text`. Do not use slash-separated text when line breaks matter.

Essential text includes title, selected quote, any secondary text, and attribution. It must remain fully readable. Image-text may be partially reflected, eroded, or obscured but must stay intentionally recognizable.

If essential Chinese is still wrong after one targeted regeneration, stop relying on another identical generation call. Ask whether to shorten the copy or use a deterministic local typesetting workflow. Do not silently switch workflows.

## Preflight

Before generating, confirm:

- source and attribution are exact;
- requested mode and image count are explicit;
- relation mode fits the source mood;
- secondary text is omitted in Preserve unless it clearly earns its place;
- any secondary text passed the fit, function, restraint, and novelty checks;
- aspect ratio has a content-based reason and paired hierarchy variants use the same canvas;
- one metaphor and one material action are locked;
- classical or restrained source quotes keep coherent optical sizing and level baselines unless the user approved disruption;
- semantic words are not enlarged, tilted, or stepped merely to illustrate their meaning;
- image-led text has a named host surface;
- type-led effects target only one or two words;
- color and composition do not repeat recent outputs;
- the metaphor does not accidentally create injury or self-harm imagery.

When red stains, body silhouettes, hanging forms, or confinement could imply injury unintentionally, move the metaphor to objects, paper, weather, or abstract collage boundaries.

## Review at two scales

At thumbnail size, check first-read hierarchy, accent visibility, density, and whether the result is recognizably image-led or type-led.

At full size, check:

- every essential Chinese character and `《》`;
- delivered width-to-height ratio matches the locked canvas family within normal generator tolerance;
- fake metadata, pseudo-Chinese, and meaningless microtext;
- paper texture and print coherence;
- reflections, shadows, gravity, perspective, and weather direction;
- whether image-text belongs to its host surface;
- whether the main quote still reads as literature rather than an advertising slogan;
- whether Preserve remains emotionally intact, Resonance adds without correcting, Tension complicates, or Satire genuinely challenges.

## Failure levels

### P0 — must regenerate

- wrong or garbled essential Chinese;
- missing title brackets;
- impossible anatomy, reflection, architecture, or object function;
- accidental injury imagery;
- wrong source, author, or requested count.
- wrong orientation or materially wrong aspect-ratio family.

### P1 — targeted regeneration

- image-led result is a picture with detached captions;
- type-led result is plain text plus a token thumbnail;
- accent is absent or washed out;
- paper disappears into a cinematic scene;
- secondary text contradicts the selected relation mode or injects unearned cynicism;
- classical or restrained source text uses unexplained diagonal baselines, staircase layout, rotation, or dramatic size jumps;
- a semantic keyword becomes a loud slogan instead of remaining inside the poem's typographic rhythm;
- composition repeats a recent result too closely.

### P2 — preference

- minor spacing, balance, or texture differences that do not break the concept.

Return a valid P2 result for comparison instead of endlessly regenerating.

## Targeted regeneration

State the single defect and lock all invariants:

`Change only [defect]. Preserve the exact text, metaphor, composition family, object placement, paper tone, accent hue, and overall density.`

Regenerate an affected variant once. If the same P0 defect remains, change strategy rather than repeating the same prompt.

## Delivery

Save every requested final image in the current project according to the active project instructions. Do not overwrite existing assets; add `-v2`, `-v3`, and so on. Report absolute paths.

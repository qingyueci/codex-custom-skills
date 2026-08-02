# Source Intake

Use this reference whenever the user supplies screenshots, photos, scans, multiple quotations, or uncertain attribution.

## Classify every input image

Choose one role:

- **Content reference:** extract the quote and attribution; do not imitate the screenshot design.
- **Style reference:** inherit selected color, typography, density, or material cues.
- **Edit target:** preserve the existing image and change only requested elements.

Do not treat a phone screenshot as a style reference unless the user asks.

For approved style references, extract reusable invariants separately: source-text alignment, baseline behavior, optical size consistency, type family, negative-space ratio, accent logic, paper depth, and image-fragment treatment. Also record the defect the user rejects. Do not copy the reference's words, title, objects, or exact layout.

## Extract separately

Record:

- exact source quote;
- poem or poster title, if explicitly supplied;
- work or book title, if explicitly supplied;
- author or attribution, if explicitly supplied;
- visible UI, watermark, account name, translation, or other non-content;
- OCR uncertainty and ambiguous characters.

Do not copy status bars, playback controls, watermarks, account names, decorative English, or translations unless requested.

## Title and attribution

- Wrap an explicitly supplied Chinese poem, article, or work title in `《》`.
- Preserve existing brackets and punctuation exactly.
- Do not invent a poster title.
- If no poster title exists, use an explicitly supplied work title only when it helps the reading; otherwise omit the title.
- Do not infer an author from a work title alone.
- Keep attribution only when explicitly provided or confidently visible and relevant.

Ask for confirmation only when OCR uncertainty changes the meaning, title, author, or requested output count. Otherwise make a conservative choice and proceed.

## Multiple sources and count

Determine the requested deliverable count before generating:

- `2+2` means four final images;
- two sources plus `再来两张` normally means one image per source;
- `每段两版` means image-led and type-led for every source;
- in Batch mode, keep each source, countertext, and filename isolated.

Never silently double the requested count because the default workflow normally creates two variants.

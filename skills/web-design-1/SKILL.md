---
name: web-design-1
description: Build, refine, verify, and deliver responsive photo, motion-photo, video, and audio storytelling websites. Use when turning a personal trip, exhibition, portfolio, event, or visual archive into an immersive web experience; when improving an existing media-heavy site; or when preparing a verified local or public release. The workflow is style-neutral and adapts to the supplied content, references, and existing design system.
---

# Web Design 1

## Purpose

Turn mixed visual media into a coherent, responsive narrative website without imposing a fixed visual style. Reuse the existing project when present, protect original media, and finish with working interactions, visual QA, and verifiable delivery.

## Operating Rules

- Inspect the existing workspace and current browser state before changing structure.
- Treat source photos, videos, motion-photo clips, audio, and generated images as read-only originals.
- Infer typography, color, spacing, motion, and composition from the brief, references, and content. Do not reuse project-specific names, palettes, copy, or assets from previous work.
- Prefer a small, maintainable implementation. Avoid decorative components that compete with the media.
- Preserve requested fidelity. Compress or transcode media only when the user asks or accepts the tradeoff.
- Never publish until the user explicitly asks. When publishing, verify the public URL and representative assets.
- For workspace changes, preserve the baseline, record the diff, verify the result, and provide a runnable rollback.

## Workflow

### 1. Establish the current state

1. Identify the active project, framework, entry files, build command, and hosting configuration.
2. Inventory media by type, dimensions, duration, codec, size, and likely chapter.
3. Detect duplicate, generated, intermediate, and source files. Do not delete sources during the design pass.
4. Reuse confirmed routes, content mappings, captions, and interactions rather than rebuilding them.
5. Capture desktop and mobile baselines before a substantial redesign.

### 2. Build the narrative model

Create a compact content map before layout work:

- opening: title, place or subject, time, and one strong visual;
- route or index: chapters in viewing order;
- chapters: one dominant image or motion moment plus supporting frames;
- generated artwork: contextual transition, inset, background layer, or editorial counterpoint;
- closing: restrained summary, credits, or return navigation.

Give every media item a role. Remove repeated images that do not add a new moment, scale, subject, or emotional beat.

### 3. Choose layout from the content

Use the media itself to determine composition:

- panoramic media: wide hero or edge-to-edge cinematic strip;
- portrait media: staggered editorial columns or paired vertical sequence;
- strong subject with negative space: place caption or subtle interaction in the existing empty area;
- action sequence: ordered frames with clear temporal labels;
- generated image: merge through shared crop, color field, mask, or adjacent rhythm; never cover a primary subject or essential caption.

Maintain hierarchy with scale, whitespace, alignment, and pacing before adding effects. Avoid card grids unless the content genuinely behaves like a catalog.

### 4. Implement media behavior

#### Still and generated images

- Use responsive image sizing and stable aspect-ratio boxes to prevent layout shift.
- Provide meaningful `alt` text for content images and empty `alt` text for decoration.
- Keep captions visible on touch devices; do not depend on hover alone.
- Lazy-load below-the-fold images, but load the leading visual eagerly.

#### Motion photos

- Use the still frame as the default visual.
- On pointer hover, preview motion muted when the device supports hover.
- On click or tap, play the full motion in place or in a focused viewer with sound.
- Ensure a second click, close action, `Escape`, and playback end restore a predictable state.
- Pause off-screen and hidden motion; never autoplay many clips simultaneously.

#### Video

- Give true videos a distinct cinematic or sequence region instead of disguising them as photos.
- Use `preload="none"` or `metadata` outside the initial viewport.
- Supply poster frames, native controls when useful, and a visible play affordance.
- Pause other media when a focused video starts.

#### Background music and sound

- Add a persistent play/pause control with a clear state label.
- Attempt default playback only after the page is ready; if the browser blocks it, show a single unobtrusive prompt that resumes on the first user gesture.
- Duck or pause background music while a motion photo or video plays with sound, then restore the previous BGM state.
- Respect device mute, reduced motion, and user choice across navigation during the session.

### 5. Add restrained interaction

Interactions should reinforce the subject or guide attention:

- use small cursor or touch responses in genuine negative space;
- prefer transform and opacity animations over layout-changing effects;
- make decorative objects keyboard-inert and screen-reader-hidden;
- provide keyboard access for controls, viewers, and chapter navigation;
- include a reduced-motion mode that removes continuous drift and parallax;
- keep touch targets at least 44 by 44 CSS pixels.

Do not scatter interactions randomly over faces, text, controls, or focal subjects. If an empty region needs support, first test crop, scale, and layout balance before adding decoration.

### 6. Tune desktop and mobile independently

Desktop and mobile should share content but not identical pacing.

- On mobile, shorten introductory blocks so the first chapter image is partially visible.
- Provide a compact horizontal chapter strip or equivalent long-page navigation.
- Keep titles and playback states persistently legible.
- Raise microcopy below 11px unless it is purely decorative.
- Prevent horizontal overflow, overlapping captions, clipped controls, and media wider than the viewport.
- Preserve safe areas for fixed controls on notched devices.

### 7. Verify before delivery

Load `references/qa-checklist.md` and complete the relevant checks. At minimum:

1. run syntax, type, lint, and build checks supported by the project;
2. reopen the built site and exercise every chapter link;
3. test still, hover preview, click playback with sound, close, and replay;
4. test BGM start, browser-blocked fallback, pause, and audio ducking;
5. inspect desktop and mobile screenshots for overlap, crop, hierarchy, and empty-space balance;
6. confirm missing assets and console errors are zero;
7. verify source media were not overwritten;
8. record exact local or public verification URLs and status codes;
9. reopen the patch, verification record, and rollback script before reporting completion.

## Delivery Format

Return:

- the runnable website path;
- the main changes by chapter or component;
- the modified artifact, patch or diff, verification record, and rollback path;
- verified desktop and mobile behaviors;
- the public URL only when a deployment was requested and verified;
- any remaining media or browser limitation in one concise note.

Stop once the requested behavior and rollback have been verified.

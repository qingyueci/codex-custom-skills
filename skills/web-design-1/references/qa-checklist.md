# Media Story Website QA Checklist

Use only the checks relevant to the current project. Record literal results rather than writing “looks good”.

## Content and structure

- [ ] Chapter order matches the intended narrative.
- [ ] Each image, motion clip, video, generated image, and audio file has a deliberate role.
- [ ] Labels match the actual action and subject.
- [ ] Generated art does not overlap a focal subject, caption, or control.
- [ ] No stale placeholder or project-internal wording is visible.

## Layout

- [ ] Desktop hero, chapter transitions, and closing have distinct hierarchy.
- [ ] Mobile first screen reveals useful content rather than only an introduction.
- [ ] No horizontal overflow at 320, 375, 390, 768, 1024, and 1440 CSS pixels.
- [ ] Fixed navigation and audio controls avoid device safe areas.
- [ ] Text remains readable over every crop and playback state.

## Interaction and accessibility

- [ ] All controls work with pointer, touch, keyboard, and visible focus.
- [ ] Motion-photo hover preview is muted; click or tap playback can use sound.
- [ ] Closing or ending playback restores captions, posters, and BGM state.
- [ ] Off-screen media pauses and does not preload unnecessarily.
- [ ] `prefers-reduced-motion` removes continuous decorative motion.
- [ ] Decorative elements are ignored by assistive technology.
- [ ] Touch targets are at least 44 by 44 CSS pixels.

## Media and performance

- [ ] Original source files remain unchanged.
- [ ] Leading visual loads eagerly; below-the-fold media loads lazily.
- [ ] Videos use posters and an intentional preload policy.
- [ ] No 404 asset requests, decoding failures, or console errors.
- [ ] Media fidelity and file-size tradeoffs match the user's decision.

## Release evidence

- [ ] Syntax, type, lint, and build commands exit successfully where available.
- [ ] Desktop and mobile screenshots were inspected after the final change.
- [ ] Baseline and modified commands, outputs, and exit statuses are recorded.
- [ ] Patch or diff reopens successfully.
- [ ] Rollback script is runnable and verified non-destructively.
- [ ] Public root and representative image, video, audio, script, and stylesheet URLs return 200 when deployed.

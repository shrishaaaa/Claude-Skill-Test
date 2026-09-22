# Hyperframes Composition Brief: SecurityPal AI Vendor Questionnaire Walkthrough

## Objective
A pixel-accurate, screenshot-driven product walkthrough of the SecurityPal AI vendor security-questionnaire flow, animated with realistic cursor interaction — not a recreated UI.

## Output
- Composition directory: `composition/`
- Rendered video: `brag.mp4`
- Format: landscape — 1920x1080
- Duration: 31.5 seconds

## Source Material
- Five real product screenshots supplied by the user (authoritative, pixel-exact reference):
  - `assets/screens/scene1-invite.png` (2000x1193) — questionnaire invitation
  - `assets/screens/scene2-check-email.png` (2000x1193) — check your email
  - `assets/screens/scene3-dashboard.png` (1820x970) — Vendor Questionnaires dashboard (patched: "OpenAI" → "VendorCorp" in the vendor table, matched font/size/baseline/color; every other pixel untouched)
  - `assets/screens/scene4-detail.png` (2000x1195) — VendorCorp questionnaire detail (dark-overlay modal)
  - `assets/screens/scene5-answer.png` (2000x1195) — question answering + comments panel (used for both Scene 5 and Scene 6 via a camera pan, since both live in the same screenshot)
- These images are used AS-IS as full-frame backgrounds. No UI is recreated in HTML/CSS/Tailwind. Any additional overlay (cursor, hover glow, typed text) is a thin synthetic layer on top, positioned to match the screenshot's own real coordinates.
- Copy that must appear verbatim: everything in the screenshots, unchanged, except the OpenAI→VendorCorp patch already baked into scene3's image asset.

## Creative Direction
- Tone preset: app-store (closest fit) — but this brief overrides the normal /brag creative laws (15-25s hook/punchline pattern, music-driven pacing). Follow the user's literal 6-scene shot list and pacing instead.
- Angle: real user, real product, real click-by-click flow. No invented screens, no invented UI, no headline text overlays beyond the small synthetic cursor/typing/hover layer described below.
- Avoid: redesigning any UI, changing existing screenshot text/fonts/colors/layout, inventing buttons, excessive zoom/blur, flashy transitions, particles, music/SFX (none requested — keep silent).

## Visual Identity
- Canvas background: light neutral (#F5F6F8) so image letterboxing/pillarboxing blends with each screenshot's own near-white background.
- Cursor: a standard OS-style pointer (white fill, dark 1.5px stroke, subtle drop shadow), ~30px, moved with human easing (not linear/robotic).
- Synthetic interaction cues (since screenshots have no baked-in hover/press state):
  - Hover: a soft rounded-rect glow (low-opacity blue) fading in over the target element's real bounding box.
  - Press: cursor scale-down (0.92) + glow intensifies briefly + small ripple ring expands and fades from the click point.
  - Typed text: Inter font matching the product's own type, placed exactly over each field's real (white) interior, same size/color as the editor's real text, with a blinking caret — never instant, ~40-45 characters/sec.
- Typography for any overlay text: Inter (400/500/600/700, self-hosted TTF, `@font-face`), matching the product's own apparent typeface family so overlays don't clash.

## Storyboard
Use `brag-plan.md` as the creative contract. Six scenes / five screenshots (Scene 5 and 6 share one image via an internal camera pan):
1. Invitation — 0-5.5s — still → cursor → hover → click "Start questionnaire"
2. Check your email — 5.5-9.5s — read pause → ambient cursor
3. Dashboard — 9.5-15.5s — VendorCorp row visible → cursor → click "View" → zoom transition
4. Questionnaire detail — 15.5-20.5s — settle from zoom → cursor scans questions → click Q1
5. Answering — 20.5-25.8s — click response field → gradual realistic typing → click "Comment on this question"
6. Add a comment — 25.8-31.5s — camera pans to comments panel → click comment box → gradual typing → click "Comment" → subtle confirmation

## Audio
None. No music, no SFX, no voiceover — silent by explicit user instruction. Do not add an ambient bed "to fill space."

## Hyperframes Instructions
Load `hyperframes-core` (composition contract), `hyperframes-animation` (cursor/hover/press motion), `hyperframes-keyframes` (the zoom/pan camera moves in Scenes 3→4 and 5→6). This is a monolithic single-file composition (5-6 sequential full-frame image scenes with overlay layers) — no sub-compositions needed for a project this size.

Requirements:
- Every scene's background image must render at its correct aspect ratio (object-fit: contain equivalent, computed per-image scale/offset) — never stretched/distorted.
- Cursor motion must use eased tweens (power2/power3), never linear "teleport" jumps.
- Hover/press/typing overlays must be pixel-positioned against the real screenshot coordinates measured from the source images (see index.html comments for the measured bounding boxes).
- Keep every text overlay legible at all times; typed text must fit on one line inside its field (content was chosen short enough to fit).
- No audio elements at all.
- Run `hyperframes check` before render — it is brag's single gate.

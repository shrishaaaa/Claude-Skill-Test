# Hyperframes Composition Brief: SecurityPal AI Full-Flow Walkthrough (v3)

## Objective
The complete, real-screens-only vendor questionnaire walkthrough (admin send-flow + vendor answer-flow), fixing the previous cut's cursor/zoom misalignment by parenting all overlay layers (cursor, hover-glow, ripple, typed text) inside each scene's own zooming wrapper, and sequencing every interaction as **zoom completes → then cursor/click/type happens** (never simultaneous), per explicit user feedback.

## Output
- Composition directory: `composition/`
- Rendered video: `brag.mp4`
- Format: landscape — 1920x1080
- Duration: ~50 seconds

## Source Material
17 of the 18 real screenshots the user added directly to the repo (`1.png`–`18.png`, all 1920x958, RGB, skip `7.png`/the mid-edit questions-editor detail): dashboard, the full "Send questionnaire" admin modal flow, the questionnaire-invite email, the vendor invitation + check-your-email pages, the sign-in email, the answer/comment flow, and the real "You're all set" completion screen. Vendor name is left as **OpenAI** — no patch this cut, per explicit instruction.

## Critical Fix From Prior Feedback
The prior cinematic cut kept cursor/hover-glow/ripple as **root-level siblings** of the per-scene zooming `.inner` wrapper, computed against pre-zoom canvas coordinates. Once a scene zoomed in, the real UI element visually moved (scale+translate on `.inner`) but the cursor did not, producing visible misalignment. This cut fixes it structurally: every scene builds its **own** cursor/glow/ripple/type-overlay elements as children of that scene's `.inner`, using the same local (pre-zoom) coordinates as the screenshot `<img>` itself — so when `.inner` scales/pans for the zoom, the overlays are carried along and stay pixel-locked to the real element at any zoom level.

Sequencing is also now strictly ordered per interaction: the zoom tween completes first; only then do the cursor fade-in, hover glow, and click/ripple play. Typing (when present) starts after the click settles.

## Creative Direction
- Same restrained cinematic language as the prior cut (110-125% zooms, no fisheye/3D/spins/particles), refined per the fix above.
- No invented UI this cut — the real "You're all set" / "Done" screen is the authentic ending; no synthetic success toast or title card needed.

## Visual Identity
Canvas backdrop #F5F6F8. Screenshots are 1920x958 → scale 1.0, letterboxed by 61px top/bottom (no distortion, no scaling artifacts). Inter self-hosted via `@font-face` for typed-text overlays (email/name/comment).

## Storyboard
See `brag-plan.md` — 17 scenes, each a real screenshot, ~50s total.

## Audio
None.

## Hyperframes Instructions
Load `hyperframes-core`, `hyperframes-animation`, `hyperframes-keyframes`. Monolithic single-file composition. Each scene is self-contained: its own `.inner` wrapper, its own cursor/glow/ripple/type-overlay DOM (built once at `document.fonts.ready` time, before the timeline registers), its own zoom-then-interact GSAP sequence.

Requirements:
- Every zoom/interaction target is a real, measured coordinate on the actual screenshot (measured directly from the PNGs via pixel analysis, not eyeballed).
- Cursor motion uses GSAP transform (`x`/`y`), never `left`/`top`.
- All overlay elements for a scene live inside that scene's `.inner` wrapper so the zoom carries them along — this is the core fix.
- Zoom tween completes before any cursor/click/type tween starts for that beat.
- Text measurement for typing-caret math happens once at build time, never inside a per-frame timeline callback.
- No audio elements.
- Run `hyperframes check` before render.

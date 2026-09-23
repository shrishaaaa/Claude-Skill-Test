# Hyperframes Composition Brief: SecurityPal AI Cinematic Walkthrough (v2)

## Objective
A more cinematic re-cut of the vendor-questionnaire walkthrough: continuous camera-follows-cursor motion (zoom in on the active element, pan between focal regions, zoom out to settle) over the same five real screenshots, no UI recreation.

## Output
- Composition directory: `composition/`
- Rendered video: `brag.mp4`
- Format: landscape — 1920x1080
- Duration: ~35.5 seconds

## Source Material
- Same five screenshots as the prior cut (reused as-is, already patched OpenAI → VendorCorp in scene3): `scene1-invite.png`, `scene2-check-email.png`, `scene3-dashboard.png`, `scene4-detail.png`, `scene5-answer.png`.
- A reference video (`0b9fe58f-vendor.mp4`) was supplied for pacing/style only — it shows a broader flow (an admin "send questionnaire" modal and two Gmail interstitials) that is NOT part of our five screenshots and must not be fabricated. Only its unhurried, deliberate pacing and its "camera settles, then moves with purpose" feel are referenced.
- Copy verbatim from the screenshots, unchanged.

## Creative Direction
- Tone: cinematic-but-restrained SaaS demo. Primary technique: **the camera follows the user's attention** — every cursor move that's about to interact with something gets a matching, proportional camera zoom/pan; every completed interaction gets a settle or a deliberate pull-back.
- Zoom range: 105-125% typical, up to ~130% for the single deepest moment (typing in the response editor). Never so far the UI blurs or an important element crops out of frame.
- No fisheye/3D/perspective distortion, no spinning, no particles, no aggressive cinematic zooms, no hard cuts where a pan/zoom transition is specified.
- One new emphasis technique this cut: a soft radial vignette (dark, low opacity, no hard edge) dims everything outside the VendorCorp row on the dashboard, then fades away — a naturalistic way to "make the rest of the dashboard less visually prominent" without touching the screenshot pixels.
- One small synthetic element this cut: a restrained white "Comment added successfully" toast with a green check, appearing only because the brief explicitly asks for a submit confirmation and no screenshot supplies one. Keep it small, on-brand (white card, soft shadow, Inter type, SecurityPal AI's own blue/green accents), never a full invented screen.
- One optional minimal title card at the very end: "Vendor Security Questionnaire — Complete" — small, centered low on the frame, plain Inter, no animation flourish beyond a simple fade.

## Visual Identity
Unchanged from the prior cut (see that brief) — canvas backdrop #F5F6F8, Inter self-hosted via `@font-face`, cursor/hover-glow/ripple/typed-text overlay mechanics reused.

## Storyboard
Use `brag-plan.md`. Nine narrative beats across five screenshot scenes (Scenes 5-9 share one screenshot via continuous camera movement, not scene cuts):
1. Start questionnaire (0-4.6s) — zoom-in click
2. Check your email (4.6-8.3s) — settle + slow zoom to headline
3. Dashboard (8.3-15.0s) — vignette-emphasized VendorCorp row → View click → zoom-transition
4. Questionnaire detail (15.0-19.6s) — zoom to Q1 → click
5. Answering (19.6-24.0s) — zoom deeper while typing the response
6. Open comments (24.0-26.6s) — zoom out to reveal comment link → click → pull back to 1.0 → push into comments panel
7. Type comment (26.6-29.2s) — typed comment in the panel
8. Submit (29.2-31.2s) — click Comment → small success toast
9. Final state (31.2-35.5s) — zoom out to the full, completed interface → minimal title card

## Audio
None — silent, matching the reference video and the brief.

## Hyperframes Instructions
Load `hyperframes-core`, `hyperframes-animation`, `hyperframes-keyframes` (zoom/pan camera language is the star of this cut). Monolithic single-file composition, same structural pattern as the prior cut, extended with more granular GSAP zoom/pan segments per scene and the vignette + toast + title-card additions.

Requirements:
- Every zoom/pan targets a real, measured coordinate on the actual screenshot — never an arbitrary/decorative camera move.
- Camera motion uses eased scale/x/y tweens on each scene's `.inner` wrapper (never the timed `.clip` element itself).
- Cursor motion continues to use GSAP transform (`x`/`y`), never `left`/`top`, to avoid non-transform-motion pixel snapping.
- Any text measurement for the typing-caret math happens once at build time (inside `document.fonts.ready`), never inside a per-frame timeline callback.
- No audio elements.
- Run `hyperframes check` before render — it is brag's single gate.

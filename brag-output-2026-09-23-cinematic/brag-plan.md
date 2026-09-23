# Brag Plan: SecurityPal AI — Cinematic Vendor Questionnaire Walkthrough (v2)

## What is this app?
SecurityPal AI's vendor security-questionnaire workflow. This is a **re-cut** of the walkthrough delivered previously (`brag-output-2026-09-22-165645/`), same five source screenshots (already pixel-patched OpenAI → VendorCorp), now choreographed as a continuous "camera follows the user's attention" cinematic demo per a new, more detailed brief and a reference video supplied for pacing/style only.

## The angle
Same literal-fidelity constraint as before — the five screenshots are the exact visual source of truth, animated in place, never redesigned. What changes in this cut: the camera actively zooms toward whatever the cursor is about to interact with (105–125% punch-ins), pans between focal regions within a single screenshot instead of hard-cutting, dims the non-active area of a busy screen (dashboard row emphasis) with a soft vignette, and closes on a deliberate zoom-out + minimal title card. The reference video (`0b9fe58f-vendor.mp4`, 29.5s) covers a broader flow (admin send-questionnaire modal, two Gmail interstitials) that isn't in our five screenshots — it's used only for its *pacing and camera-follow feel*, not as additional source screens to fabricate.

## Hook (first 2-3 seconds)
Full, still frame of "Acme Corp has sent you a security questionnaire" — no invented headline, the real page is the hook.

## Key moments (the middle)
- Zoom-in click on "Start questionnaire"
- Check-your-email beat, camera settles on the message
- Dashboard: VendorCorp row emphasized (vignette + zoom), View clicked
- Questionnaire detail: camera zooms to Q1
- Answering: zoom deeper into the editor while typing
- Zoom-out to comment link, pan to the comments panel (no hard cut), typed comment
- Submit → small success confirmation
- Deliberate zoom-out to the full, completed interface + minimal title card

## Outro / punchline
Camera settles wide on the completed questionnaire (response + comment both visible), fades in a small, minimal title: "Vendor Security Questionnaire — Complete." No dramatic sting.

## User flow worth showing
Same as before — Acme Corp sends → vendor invited → checks email → opens SecurityPal AI dashboard → opens VendorCorp's questionnaire → reviews Q1 → answers it → comments on it → submits → done. Every beat uses the real screen; the only addition this cut is the camera language.

## Tone
- Preset: `app-store` / `cinematic` hybrid — the brief explicitly asks for "cinematic SaaS product walkthrough" while staying restrained (no fisheye, no 3D, no dramatic spins, no particles).
- Creative direction: continuous camera-follows-cursor motion is the primary technique, not cuts. 105–120% zooms (occasionally to ~130% for the deepest in-editor moment), always centered on the real element being used.
- Interpretation: pacing stays "professional and easy to follow" (per brief) — slower and more deliberate than a punchy hook reel, matching the reference video's unhurried demo pacing rather than the usual /brag 15-25s law.

## Format: landscape — 1920x1080
## Duration: ~35.5 seconds (9 scenes; longer than the default law by explicit, repeated user instruction)

## Visual identity (from the source screenshots — untouched)
Same as the previous cut: white/#F9FAFB app chrome, #0B5FE0-ish blue accent, Inter-like type. Canvas backdrop #F5F6F8 for letterboxing. New this cut: a soft radial vignette (dark, low-opacity) used once to emphasize the VendorCorp dashboard row, and one small synthetic "success" toast (white card, green check, Inter text) for the comment-submission confirmation — the only screenshot moment without a supplied "success" reference image, kept deliberately minimal per the brief's own instruction ("a small, professional confirmation animation is enough").

## Share copy (draft)
A cinematic look at the SecurityPal AI vendor questionnaire flow — camera follows every click, hover, and keystroke from invite to submitted answer.

## Audio direction
None — silent, matching the reference video (no audio track) and the brief (no mention of music/SFX/voice).

## Storyboard

### Scene 1 — Start questionnaire — 0.0-4.6s
Screenshot: `scene1-invite.png`. Still 1.3s → cursor eases to "Start questionnaire" while camera slowly punches in (1.0→1.1) on the button → hover glow → click/ripple → zoom continues into the transition.
Audio: none. Transition: zoom-continuation crossfade → Scene 2.

### Scene 2 — Check your email — 4.6-8.3s
Screenshot: `scene2-check-email.png`. Settle from the incoming zoom → hold → slow zoom (1.0→1.1) toward the "Check your email" headline/icon with a light ambient cursor drift → crossfade out.

### Scene 3 — SecurityPal AI dashboard — 8.3-15.0s
Screenshot: `scene3-dashboard.png`. Full dashboard → cursor moves toward the VendorCorp row → camera zooms (1.0→1.22) and a soft vignette dims everything outside the row → View hover/click → zoom continues toward the row/button as the scene crossfades out (the "zoom into clicked element → cross-transition" pattern from the brief).

### Scene 4 — VendorCorp questionnaire — 15.0-19.6s
Screenshot: `scene4-detail.png`. Settle from incoming zoom → brief hold to read the layout → cursor + camera move/zoom (1.0→1.15) toward Q1 ("How often is the Acceptable Use Policy...") → hover/click → zoom continues into the transition.

### Scenes 5-9 — Answering through completion — 19.6-35.5s (single screenshot, continuous camera move — `scene5-answer.png`)
One continuous shot, no further hard cuts, matching the brief's "camera should smoothly move/zoom... not simply cut":
- **5. Answering (19.6-24.0s):** settle already-zoomed on the question/editor → cursor clicks the response field → camera creeps in further (1.1→1.25) while a realistic typing animation enters: "We review the Acceptable Use Policy quarterly and after any significant changes to our systems or processes."
- **6. Open comments (24.0-26.6s):** zoom back out slightly to reveal "Comment on this question" → hover/click → brief full pull-back to 1.0 as the pivot, then camera pushes into the right-side comments panel (1.0→1.2).
- **7. Type comment (26.6-29.2s):** cursor clicks the empty comment box → typing animation: "This is aligned with our current security roadmap."
- **8. Submit (29.2-31.2s):** cursor to "Comment" → hover/click/ripple → small synthetic success toast ("Comment added successfully") fades in near the panel, restrained, no confetti.
- **9. Final state (31.2-35.5s):** camera zooms back out to the full interface (response + comment both visible), settles, and a minimal title card fades in low on the frame: "Vendor Security Questionnaire — Complete."

**Audio summary:** none — silent throughout, matching both the reference video and the brief.

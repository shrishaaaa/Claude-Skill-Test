# Brag Plan: SecurityPal AI — Full Vendor Questionnaire Flow (v3)

## What is this app?
SecurityPal AI's complete vendor security-questionnaire workflow, both sides: an Acme Corp admin sends a questionnaire to a vendor, and the vendor receives, signs in, answers, comments, and submits it.

## The angle
This is the definitive, complete cut. The previous two cuts worked from a partial 5-screenshot subset; the user has now supplied 18 real screenshots covering the entire flow end to end, matching the actual reference video far more closely. This plan uses 17 of them as sequential real screens (one, the mid-edit "questions editor" detail, is skipped to keep pacing tight — it's a secondary detail, not a flow beat).

**Explicit fix from user feedback on the previous cut:** the camera must zoom in *before* the cursor moves/clicks/types (not simultaneously), and every cursor/hover/click/typed-text overlay must be pixel-locked to the real UI element even while the camera is zoomed — the previous cut's cursor was a shared root-level layer that didn't move with the per-scene zoom transform, so at high zoom the cursor drifted off the actual button. This cut fixes that architecturally: the cursor, hover-glow, ripple, and any typed-text overlay are children of the same zooming `.inner` wrapper as the screenshot image in every scene, so they scale and pan together and stay locked to the real element at any zoom level.

**Vendor name:** left as **OpenAI**, exactly as captured — no pixel patch this time (explicit user instruction).

## Hook (first 2-3 seconds)
The real Vendor Questionnaires dashboard, full and still, before the camera moves.

## Key moments (the middle)
- Admin sends a questionnaire: dashboard → "Send questionnaire" → pick a vendor → fill contacts/due date/template → send
- Vendor gets the email → opens the invitation link → signs in with name/email → checks email → clicks the sign-in link
- Vendor answers Q1, comments on it, submits the comment
- Vendor reaches the final question and sees the real "You're all set" completion screen

## Outro / punchline
No invented title card this time — the real "You're all set" modal and its "Done" button are the authentic ending; the flow simply settles there.

## User flow worth showing
The complete real loop: Acme Corp admin sends → vendor invited by email → vendor signs in → vendor answers and comments → vendor is done. Every beat is a real, unaltered screen; only the camera and cursor overlays are synthetic.

## Tone
- Preset: cinematic camera-follow, refined per explicit feedback: **zoom completes first, then the interaction happens** (click, or click-then-type), never simultaneous.
- Zoom range: 110-125% typical.
- No fisheye/3D, no spins, no particles.

## Format: landscape — 1920x1080
## Duration: ~50 seconds (17 real screens, longer than the default law by explicit, repeated user instruction — this is a full walkthrough, not a teaser)

## Visual identity (from the source screenshots — untouched)
White/#F9FAFB SecurityPal AI app chrome and Gmail chrome, both used as captured. Canvas backdrop #F5F6F8 (screenshots are 1920x958, letterboxed top/bottom by 61px — close enough to the app's own near-white background to be unobtrusive).

## Share copy (draft)
The complete SecurityPal AI vendor questionnaire flow, start to finish — sending it, receiving it, answering it, and submitting it — captured end to end.

## Audio direction
None — silent, consistent with both prior cuts and the reference video.

## Storyboard (17 scenes, real screens only)

1. **Dashboard** (s1) — zoom to "Send questionnaire" → click.
2. **Send questionnaire — pick a vendor** (s2) — zoom to the vendor dropdown → click (opens it).
3. **Vendor search dropdown** (s3) — zoom stays on the list → click the top result.
4. **Vendor + assessment selected** (s4) — zoom to "Next" → click.
5. **Contacts/due date/template — empty** (s5) — zoom to the contacts field → typed email.
6. **Contacts/due date/template — filled** (s6) — zoom across due date → template → "Send to vendor" → click.
7. **Gmail — questionnaire email** (s8) — zoom to "Complete Questionnaire" → click.
8. **Invitation — empty** (s9) — zoom to Full name → typed name; zoom to Work email → typed email.
9. **Invitation — filled** (s10) — zoom to "Start questionnaire" → click.
10. **Check your email** (s11) — hold, gentle zoom on the message.
11. **Gmail — sign-in link** (s12) — zoom to "Sign in to Vendor Portal" → click.
12. **Answer Q1 — unanswered** (s13) — zoom to "Yes" → click.
13. **Answer Q1 — answered** (s14) — zoom to "Comment on this question" → click.
14. **Comments panel — empty** (s15) — zoom to the comment box → typed comment.
15. **Comment typed, button active** (s16) — zoom to "Comment" → click.
16. **Comment posted** (s17) — hold on the posted comment.
17. **Completion** (s18) — zoom out to the "You're all set" modal → zoom to "Done" → click → settle.

**Audio summary:** none — silent throughout.

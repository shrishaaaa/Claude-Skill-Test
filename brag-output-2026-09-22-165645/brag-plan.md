# Brag Plan: SecurityPal AI — Vendor Security Questionnaire Workflow

## What is this app?
SecurityPal AI: the platform vendors use to receive, answer, and collaborate on security questionnaires sent by their customers (here, Acme Corp).

## The angle
This is a **literal, pixel-accurate product walkthrough**, not a punchy hook video. The user supplied five exact screenshots as the authoritative UI reference and a full shot-by-shot script. This plan follows that brief directly rather than inventing a new creative angle: the five screenshots are animated in place (cursor moves, hovers, clicks, typing, camera pans) — no UI is redesigned, regenerated, or invented.

**Deliberate deviation from the usual /brag creative laws:** the normal 15–25s "hook → highlights → punchline" pattern is overridden by explicit user instruction. This is a 6-scene, ~31.5s demo paced for comprehension ("fast enough to maintain attention, slow enough to understand every interaction"), not a social teaser.

**One sanctioned content change:** every instance of the vendor name in the workflow is **VendorCorp**, not OpenAI. The dashboard screenshot's "OpenAI" table cell was pixel-patched to "VendorCorp" (matched font: Inter SemiBold, same size/baseline/color as the surrounding row) — everything else in that screenshot is untouched. The two later screenshots (questionnaire detail, answering screen) already show "VendorCorp" natively.

## Hook (first 2-3 seconds)
A completely still frame of "Acme Corp has sent you a security questionnaire" for ~1.5s (per spec) — the invitation itself is the hook, not an invented headline.

## Key moments (the middle)
- Cursor hovers and clicks "Start questionnaire" (Scene 1)
- Check-your-email confirmation (Scene 2)
- Dashboard reveal — VendorCorp's questionnaire, click "View" (Scene 3)
- Questionnaire detail — reviewing the question list, opening Q1 (Scene 4)
- Answering Q1 live with realistic gradual typing (Scene 5)
- Adding a comment and submitting it (Scene 6)

## Outro / punchline
No invented outro card — the video ends on the submitted-comment confirmation, per the brief ("show a subtle confirmation that the comment has been submitted... do not create dramatic animations").

## User flow worth showing
Acme Corp sends questionnaire → vendor receives invitation → vendor checks email → questionnaire appears in SecurityPal AI → VendorCorp questionnaire opened → vendor reviews questions → vendor enters an answer → vendor adds a comment. This *is* the video — every scene is a beat of this flow, using the real screens.

## Tone
- Preset: `app-store` (closest match: smooth, feature-card clean, corporate but not boring)
- Creative direction (user-specified, verbatim intent): "Premium enterprise SaaS product demo — ultra-clean, restrained, realistic cursor, minimal effects, no cinematic flourish"
- Interpretation: pacing stays measured and legible throughout; motion is restrained (0.3–0.6s eases, no bounce/overshoot beyond a subtle button press); no music-driven cuts — this is a silent, cursor-driven demo, not a beat-synced hook reel

## Format: landscape — 1920x1080
## Duration: 31.5 seconds (see deviation note above)

## Visual identity (from the source screenshots — untouched)
- Background: white / #F9FAFB (SecurityPal AI app chrome)
- Accent: #0B5FE0-ish blue (primary buttons, links, focus rings)
- Text: near-black (#111827 / #1F1F1F) headings, gray-500/600 secondary text
- Display/body font: Inter (matches the product's own UI; used for all overlay elements — cursor labels, typed-text simulation — so nothing new clashes with the screenshots)
- Strongest visual element: the actual product screens themselves — no recreated UI

## Share copy (draft)
See a vendor answer a SecurityPal AI security questionnaire end to end — invite, sign-in, dashboard, and a live answer — in under 35 seconds.

## Audio direction
- Role: **none** — the user's brief specifies no music, no SFX, no narration; this is a silent, cursor-driven enterprise product demo (`--no-music --no-sfx` equivalent, by explicit instruction: "Effects: Subtle only... no unnecessary animations", audio not requested anywhere in the brief)
- Music: none
- SFX: none
- Audio-reactive treatment: none
- Restraint rule: no audio track at all — silence is the correct creative choice here, not a fallback

## Storyboard

### Scene 1 — Questionnaire invitation — 0.0-5.5s (5.5s)
Screenshot: `scene1-invite.png` ("Acme Corp has sent you a security questionnaire", Jane Vendor / jane@vendor.com pre-filled, "Start questionnaire" button).
- 0.0-1.6s: completely still (per spec).
- 1.6-3.0s: cursor fades in near top-left of content, glides smoothly to the "Start questionnaire" button (eased, human path, not a straight linear snap).
- 3.0-3.4s: hover state — soft blue glow ring fades in around the button.
- 3.4-3.9s: press (cursor scales down slightly, button dims a touch) → release → small ripple fades out from the click point.
- 3.9-5.5s: crossfade to Scene 2.
Sequential/interaction: cursor move → hover → press → release, single continuous gesture.
Transition mood: clean crossfade → Scene 2.

### Scene 2 — Check your email — 5.5-9.5s (4.0s)
Screenshot: `scene2-check-email.png`.
- 5.5-7.0s: crossfade in, hold still (reading time).
- 7.0-8.7s: cursor drifts naturally near the envelope icon/copy (ambient, not a click — nothing to click on this screen).
- 8.7-9.5s: crossfade to Scene 3.
Sequential/interaction: none (ambient cursor only, per spec — no fake email client invented).
Transition mood: short professional fade → Scene 3.

### Scene 3 — SecurityPal AI dashboard — 9.5-15.5s (6.0s)
Screenshot: `scene3-dashboard.png` (patched: OpenAI → VendorCorp).
- 9.5-10.5s: crossfade/slide in, full dashboard visible — the VendorCorp row (top of table, "In progress", 1/5) is immediately visible, making it clear a new questionnaire has arrived.
- 10.5-12.3s: cursor glides down to the VendorCorp row, settles near the "View" button.
- 12.3-12.7s: hover state on "View" (soft glow).
- 12.7-13.2s: press/click, ripple.
- 13.2-15.5s: gentle zoom-in centered on the VendorCorp row/button, crossfading into Scene 4 (zoom + fade combined, per spec "smooth zoom/transition into the questionnaire detail screen").
Sequential/interaction: cursor move → hover → click → zoom-transition.
Transition mood: cursor clicks View → smooth zoom → Scene 4.

### Scene 4 — VendorCorp questionnaire detail — 15.5-20.5s (5.0s)
Screenshot: `scene4-detail.png` (dark-overlay modal, question list, Q1 already showing the saved answer as reference content — this is the "review" screen).
- 15.5-16.5s: settle in from the zoom (slight scale-down to rest, 1.06 → 1.0).
- 16.5-18.7s: cursor moves down over the question list, settling on Q1 ("How often is the Acceptable Use Policy reviewed and updated?").
- 18.7-19.2s: hover, then click on Q1.
- 19.2-20.5s: crossfade to Scene 5.
Sequential/interaction: cursor scans the list → click Q1.
Transition mood: question click → smooth transition → Scene 5.

### Scene 5 — Answering the questionnaire — 20.5-25.8s (5.3s, local 0.0-5.3 of the combined Scene 5/6 shot)
Screenshot: `scene5-answer.png` (same image continues through Scene 6 — see camera-pan note below).
- 20.5-21.3s: crossfade in on the left/center (question + empty response editor).
- 21.3-22.1s: cursor moves into the response textarea, clicks (focus ring already present in the screenshot's editor border, reinforced by a subtle glow).
- 22.1-24.3s: realistic gradual typing overlay: "The Acceptable Use Policy is reviewed and updated annually…" appears character-by-character (~45 cps, natural, blinking caret) into the exact placeholder position — not instant, not the full saved answer, a believable partial-then-continuing type (matches "no unrealistic instant text generation").
- 24.3-24.9s: brief hold (read the entered text).
- 24.9-25.8s: cursor moves to "Comment on this question", hover, click — begins the pan into Scene 6.
Sequential/interaction: click field → type → click comment link.
Transition mood: click comment → camera pan right (not a hard scene cut — same screenshot).

### Scene 6 — Add a comment — 25.8-31.5s (5.7s, local 5.3-11.0 of the combined shot)
Same screenshot (`scene5-answer.png`), camera pans/zooms from the left editor to the right-side Comments panel (Jane Vendor's existing comment already visible for context, per the real screenshot).
- 25.8-27.0s: camera settles on the comments panel (gentle pan + slight scale, ~1.08x, centered on the comment box).
- 27.0-27.8s: cursor moves into the empty comment box, clicks.
- 27.8-29.3s: realistic gradual typing overlay: "Reviewed and confirmed — thanks!" into the comment box (~45 cps, blinking caret).
- 29.3-30.1s: cursor moves to the "Comment" button, hover state (button brightens from its disabled gray to active blue — synthetic overlay, since the screenshot shows it disabled/gray pre-typing).
- 30.1-30.6s: press, ripple.
- 30.6-31.5s: subtle confirmation — the typed comment's cover fades to a small "posted" checkmark pulse near the button (restrained, no confetti/particles per the negative prompt), then hold on final frame.
Sequential/interaction: click box → type → click Comment → confirm.
Transition mood: soft hold → end (no outro card, per spec).

**Audio summary:** none — silent demo throughout, by explicit brief.

# Hyperframes Composition Brief: SecurityPal AI — Vendor Questionnaire Flow

## Objective
Create a short, clean, app-store-style launch video for SecurityPal AI's vendor security-questionnaire flow.

## Output
- Composition directory: `composition/`
- Rendered video: `../brag.mp4`
- Format: landscape — 1920x1080
- Duration: ~19 seconds (15-25s range)

## Source Material
- Project root: repo root (screenshots at top level, no marketing site — this is a real, in-use SaaS app)
- Primary files read: `1.png`, `5.png`, `6.png`, `8.png`, `9.png`, `10.png`, `13.png`, `18.png` (copied into `assets/screens/` with descriptive names)
- Product name: SecurityPal AI
- Tagline / strongest claim: none invented — the real product flow (send → receive → answer → done) is the claim
- Key UI or visual moment to recreate: the real screens themselves, unaltered — dashboard, send-questionnaire modal, Gmail invite, vendor sign-in, question screen, completion modal
- Copy that must appear verbatim (from the real screenshots, do not alter):
  - "Vendor Questionnaires"
  - "Send questionnaire"
  - "Send to vendor"
  - "Complete Questionnaire" (Gmail button)
  - "Start questionnaire"
  - "You're all set"

## Creative Direction
- Tone preset: app-store
- Creative direction: clean B2B feature reel — a security-compliance SaaS product shown doing exactly what it promises, cut like a crisp App Store preview rather than a screen recording.
- Interpretation: title-case feature labels, one short label + one supporting line per scene, smooth slide/wipe transitions (0.35-0.45s), no aggression, no jokes at the product's expense.
- Angle: A tight, feature-card-style walkthrough of the real product loop, told in four beats — send it, they get it, they answer it, it's done. Every frame is a real, unaltered screen; only overlay labels, cursor, and camera motion are synthetic.
- Hook: the real Vendor Questionnaires dashboard, full and still (6 requested / 5 in progress / 3 completed), before any camera motion.
- Outro / punchline: the real "You're all set" completion modal, with a SecurityPal AI logo/wordmark lockup and the line "Questionnaires, closed out." underneath.
- Avoid:
  - Generic SaaS language ("streamline your workflow" etc.)
  - Abstract filler visuals
  - Unrelated visual redesign of the real screens — keep them pixel-accurate

## Visual Identity
- Background: near-white app chrome `#FFFFFF` / `#F9FAFB`; canvas backdrop `#F5F6F8` behind screenshots (captured at 1920x958 — use a soft blurred/extended backdrop to fill the small letterbox, not flat bars)
- Text: near-black `#111827` for overlay headings, `#6B7280` for supporting lines — matches the app's own type color
- Accent: SecurityPal AI's UI blue, roughly `#0B5FFF` (matches the real "Send questionnaire" / "Start questionnaire" buttons and "In progress" pill) — use for overlay label accents so they feel native
- Display font: clean geometric/humanist sans (Inter or system-ui stack) for overlay labels
- Body font: same family, regular weight
- Visual references from the project: the dashboard's colored status pills + progress bars (hook); the "You're all set" modal (outro)

## Storyboard
Use `brag-plan.md` as the creative contract. Scene summary:
1. Dashboard hook — 3s — full still dashboard, gentle push-in starting at the end
2. Send it — 4.5s — open "Send questionnaire" modal, type a vendor contact email, click "Send to vendor"; label "Send it"
3. They get it — 4.5s — Gmail invite → click "Complete Questionnaire" → vendor invitation screen, type name + email, click "Start questionnaire"; label "They get it"
4. They answer it — 4s — real question screen, click "Yes"; label "They answer it"
5. Outro: done — 3s — real "You're all set" modal settles, SecurityPal AI wordmark + "Questionnaires, closed out." fades in, hold

Screenshot files (in `assets/screens/`):
- `01-dashboard.png` → Scene 1
- `02-send-empty.png` → Scene 2 (modal open, empty vendor-contacts field)
- `02-send-filled.png` → Scene 2 (contacts/date/template filled, ready to send)
- `03-gmail-invite.png` → Scene 3 (Gmail message with "Complete Questionnaire")
- `03-invite-empty.png` → Scene 3 (vendor invitation form, empty)
- `03-invite-filled.png` → Scene 3 (vendor invitation form, filled)
- `04-question-unanswered.png` → Scene 4
- `05-done.png` → Scene 5

## Audio
- Audio role: sparse, professional accents over a light upbeat business bed
- Audio arc: bed fades in under the hook, holds steady confidence through the send/receive/answer beats (two clicks nudged toward strong cues), single success chime as the outro modal settles, bed fades out clean
- Music: `assets/music/happy-beats-business-moves-vol-9-by-ende-dot-app.mp3` (already copied)
- Music treatment: start ~0.3 volume under the hook, hold through the middle, fade to 0 under the outro hold rather than a hard stop
- Music cue guidance: bundled preset — `<skill-dir>/assets/music/cues/happy-beats-business-moves-vol-9-by-ende-dot-app.music-cues.json` (114.84 BPM). Strong cues at 6.34s and 10.54s in the 0-25s window — nudge the "Send to vendor" click (end of Scene 2, ~7.5s) and the "Start questionnaire" click (end of Scene 3, ~12s) toward these within ±0.15s if it doesn't hurt pacing. Beat grid is dense/even (~0.52-0.55s) — fine for single-click accents, not used for any sequential-text reveal (none planned).
- Audio-reactive treatment: subtle — the dashboard hook's ambient glow/card presence or the outro wordmark may breathe slightly with music RMS; no waveform/equalizer visuals, no strobing
- Audio-coupled moments:
  - Scene 2 — typed vendor-contact email — key-tick texture, then a click on "Send to vendor"
  - Scene 3 — typed full name + work email — key-tick texture, then a click on "Start questionnaire"
  - Scene 4 — click on "Yes" — single confident click, most "it just works" beat
  - Scene 5 — modal settle — single success chime, no click needed
- SFX selection guidance: `interface/click_*` or `ui/click1`/`mouseclick1` for button taps; `keyboard/keypress-*.wav` randomized per keystroke for the two typed fields; `impact/impactBell_heavy_000` for the single outro success chime. All at app-store's 0.65-0.75 SFX volume range per `audio.md`.
- SFX analysis guidance: `<skill-dir>/assets/sfx/sfx-analysis.md` — prefer low/medium HF-risk files since this is a polished, repeated-click video
- Exact SFX choice: Hyperframes should pick exact files/timestamps/density once the animation timing is implemented; candidates already copied into `assets/sfx/` (interface clicks, ui clicks, 8 keypress WAVs, one impact bell)
- Audio files: already copied into `composition/assets/music/` and `composition/assets/sfx/`

## Hyperframes Instructions
Load the composition-building Hyperframes domain skills — `hyperframes-core`, `hyperframes-animation`, `hyperframes-creative`, `hyperframes-keyframes`, `hyperframes-cli`. /brag is its own workflow: do not enter the `hyperframes` entry-point intent interview and do not route into its generic promo / launch-video workflow. Prefer native Hyperframes conventions over anything in `/brag`.

Requirements:
- Show real UI from the source project in every scene (all screenshots above are real, unaltered captures).
- Keep all text readable in the final render.
- Keep the video within 15-25 seconds.
- Include the planned music/SFX layer (not disabled, not silent by design).
- Treat `/brag` audio notes as guidance, not a fixed cue sheet — choose exact SFX after the visual animation exists.
- Treat music cue metadata as optional timing hints; ignore cues that hurt readability, pacing, or story. Use at most 1-3 strong-cue locks.
- Use SFX to support motion/interaction: click/select sounds for real clicks, key-tick sounds for typed fields, one success cue for the outro landing.
- Honor the fade-in/fade-out music treatment.
- Consider a subtle audio-reactive touch per `hyperframes-creative` guidance — RMS/bass on an existing glow or card-presence element, not a waveform/visualizer.
- Use local assets already copied into `composition/assets/`.
- Run `hyperframes check` before render — it is brag's single gate.

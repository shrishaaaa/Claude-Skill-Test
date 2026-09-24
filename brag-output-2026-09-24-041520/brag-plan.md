# Brag Plan: SecurityPal AI — Vendor Questionnaire Flow

## What is this app?
SecurityPal AI is a platform for running vendor security questionnaires end to end: an Acme Corp admin sends a questionnaire to a vendor, and the vendor signs in, answers it, and finishes — all tracked from one dashboard.

## The angle
A tight, feature-card-style walkthrough of the real product loop, told in four beats: send it, they get it, they answer it, it's done. No invented copy, no mockups — every frame is a real, unaltered screen from the app (and the Gmail/vendor-portal screens the flow touches), cut together like a clean product demo reel rather than a screen recording. This is a different cut from the longer cinematic full-flow walkthrough already in this repo: short, punchy, scored, and built for a quick share rather than a full tutorial.

## Hook (first 2-3 seconds)
The real Vendor Questionnaires dashboard, full and still — six requested, five in progress, three completed, real vendor rows (OpenAI, Google Cloud, Airtable...). No overlay yet. This is the proof: a real, working, in-use SaaS product, not a landing page.

## Key moments (the middle)
- **Send it** — admin opens "Send questionnaire," picks a vendor, fills contact/due date/template, clicks "Send to vendor."
- **They get it** — vendor receives the Gmail invite, opens the link, signs in with name + email, clicks "Start questionnaire."
- **They answer it** — vendor lands on Q1, selects an answer, and the flow moves toward the finish.

## Outro / punchline
The real "You're all set" completion modal — the vendor's progress is saved, the loop closes itself. Land on the SecurityPal AI logo lockup with a short CTA-style line under it, in the app-store outro register.

## User flow worth showing
Entry → key action → result, exactly as the product delivers it:
1. Entry: admin's dashboard, seeing the state of every questionnaire in flight.
2. Key action: admin sends a questionnaire → vendor receives it by email → vendor signs in and starts answering.
3. Result: the vendor finishes a question and the flow settles on "You're all set."

## Tone
- Preset: **app-store**
- Creative direction: clean B2B feature reel — a security-compliance SaaS product shown doing exactly what it promises, cut like a crisp App Store preview rather than a demo recording.
- Interpretation: title-case labels, feature-card structure (one short label + one supporting line per scene), smooth slide/wipe transitions (0.35-0.45s), no aggression, no jokes at the product's expense. Confidence comes from clean pacing and real UI, not from hype copy.

## Format: landscape — 1920x1080
## Duration: ~19 seconds

## Visual identity (from the project)
- Background: near-white app chrome, `#FFFFFF` / `#F9FAFB` panel surfaces; canvas backdrop `#F5F6F8` behind the screenshots (they're captured at 1920x958, so a soft blurred backdrop fills the letterbox rather than flat bars).
- Accent: SecurityPal AI's UI blue, roughly `#0B5FFF` (primary buttons: "Send questionnaire," "Start questionnaire," progress bars, "In progress" status pill), plus status green (`Completed`) and status red (`Overdue`) used only where they appear on-screen already.
- Text: near-black `#111827` for headings, `#6B7280` gray for secondary copy — matches the app's own type color.
- Display font: clean geometric/humanist sans (Inter/system-ui family, matching the app's own UI type) for any overlay labels, so overlays feel native to the product rather than bolted on.
- Body font: same family, regular weight, for supporting lines.
- Strongest visual element: the dashboard's status table (colored status pills + progress bars) as the hook, and the "You're all set" modal as the authentic, unforced outro.

## Share copy (draft)
Send a security questionnaire. They get it, sign in, answer it, done — SecurityPal AI, start to finish.

## Audio direction
- Role: sparse, professional accents over a light, upbeat business bed — confident but restrained, never loud enough to compete with the UI.
- Music: `happy-beats-business-moves-vol-9-by-ende-dot-app.mp3` (114.84 BPM, clean even beat grid, corporate-upbeat character fits app-store energy).
- Music treatment: starts at low-medium volume under the hook, a touch of lift going into the "send" and "sign-in" beats, gentle fade-out under the outro card rather than a hard stop.
- Music cue guidance: preset cues read from `happy-beats-business-moves-vol-9-by-ende-dot-app.music-cues.json`. Strong cues at 6.34s and 10.54s land close to the "send to vendor" click (~scene 2 end, ~7s) and the "start questionnaire" click (~scene 3 end, ~11s) — worth nudging those clicks to land within ~150ms of those beats. Beat grid is dense and even (~0.52-0.55s spacing) — fine for accenting individual clicks, not for a rapid sequential-text reveal (none is planned here).
- Audio-reactive treatment: none — keep the UI the star; no waveform or glow pulsing.
- SFX posture: moderate. One soft UI click per real click/tap in the storyboard, a light key-tick texture under the two short typed fields, and a single clean "success" chime (interface `bong`/`switch` family) under the "You're all set" modal landing.
- Audio-coupled moments: the vendor-contact email field typed in scene 2, the name/email fields typed in scene 3, and the click on "Yes" in scene 4 — sound matches the action, not decoration on top of it.
- Restraint rule: never let music or SFX outrun the on-screen action — every sound is triggered by something the viewer sees happen (a click, a keystroke, a modal appearing), nothing plays speculatively.

## Storyboard

### Scene 1 — Dashboard hook — 3s
Full, still Vendor Questionnaires dashboard (real screen: SecurityPal AI, Acme Corp, 6 requested / 5 in progress / 3 completed, vendor rows including OpenAI). Hold before any camera motion so the real product reads clearly first, then a light push-in begins as the scene ends.
Sequential/interaction: none — this is the establishing hold.
Audio intent: music fades in under a calm, confident open; no SFX yet.
Audio-coupled idea: none.
Music: upbeat business bed, low volume, fading in.
Transition mood: clean slide → Scene 2

### Scene 2 — Send it — 4.5s
Zoom to "Send questionnaire," click to open the modal. Inside the modal: cursor types a vendor contact email into the field, then a quick beat on due date + template, then clicks "Send to vendor." Small feature-card label: "Send it" / "Pick a vendor, set a due date, send."
Sequential/interaction: yes — click "Send questionnaire" → type email → click "Send to vendor" (single simulated interaction chain, not a list reveal).
Audio intent: soft click on open, light key-tick texture while typing, a slightly firmer click/whoosh on "Send to vendor" as the beat lands.
Audio-coupled idea: typed email with subtle key ticks; click matched to the send action.
Music: bed continues, gentle lift approaching the strong cue near 6.3-6.5s.
Transition mood: smooth wipe → Scene 3

### Scene 3 — They get it — 4.5s
Cut to the real Gmail inbox screen, click "Complete Questionnaire," then the vendor invitation screen: cursor types a full name and work email, clicks "Start questionnaire." Label: "They get it" / "One email, one link, no account needed."
Sequential/interaction: yes — click email CTA → type name → type email → click "Start questionnaire."
Audio intent: a light "mail" click, two short key-tick bursts for the two fields, a clean click on "Start questionnaire" ideally landing near the ~10.5s strong cue.
Audio-coupled idea: typed name/email with key ticks; click matched to the CTA.
Music: bed holds steady energy through this beat.
Transition mood: smooth wipe → Scene 4

### Scene 4 — They answer it — 4s
The real vendor question screen ("1. Is your company located in the US?"). Cursor moves to "Yes" and clicks it. Label: "They answer it" / "Answer, comment, keep moving."
Sequential/interaction: yes — single click on the "Yes" option.
Audio intent: one confident, satisfying click — this is the most "product working" beat, give it a touch of presence.
Audio-coupled idea: click matched exactly to the option selecting.
Music: bed sustains, no extra swell — let the click read clearly.
Transition mood: soft crossfade → Scene 5

### Scene 5 — Outro: done — 3s
The real "You're all set" completion modal, centered and settled (no further clicking needed — it's the natural end state). SecurityPal AI logo lockup fades in beneath/beside it with the line "Questionnaires, closed out." Hold.
Sequential/interaction: none — settle and hold.
Audio intent: one clean success chime as the modal is already on screen/settles, then music fades under and out.
Audio-coupled idea: single chime timed to the hold, not to any click (no click needed here).
Music: fades out under the hold, ending clean rather than cutting off.
Transition mood: hold to end.

**Music mood for this video:** upbeat, clean, corporate-confident throughout — no drop, no chaos, steady lift and a gentle fade at the end.
**Audio summary:** A light business-pop bed runs under the whole cut at restrained volume, accented only by real UI sounds (clicks, key ticks) tied to what's actually happening on screen, closing on a single success chime as the flow completes and the bed fades out.

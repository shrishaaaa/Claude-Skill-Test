# Hyperframes Composition Brief: Questionnaire Dashboard

## Objective
Create a short launch-style brag video for the Questionnaire Dashboard — a SaaS dashboard that tracks and manages security/compliance questionnaires in one searchable, sortable table.

## Output
- Composition directory: `brag-output/composition/`
- Rendered video: `brag-output/brag.mp4`
- Format: landscape — 1920x1080
- Duration: 21 seconds

## Source Material
- Project root: uploaded component `/root/.claude/uploads/139125f4-4c96-5323-be27-b17be1c79696/30fc4f70-QuestionnaireDashboard.tsx` (single React/TypeScript component, Tailwind CSS, lucide-react icons — no live URL, no broader app)
- Primary file read: `QuestionnaireDashboard.tsx` (the only project artifact)
- Product name: Questionnaire Dashboard
- Tagline / strongest claim: "Track and manage all your questionnaires in one place." (from the component's own header subtext)
- Key UI or visual moment to recreate: the full table — search bar, status badges (colored pill + dot), assignee avatar chips (colored initials), sortable column headers, "New Questionnaire" primary button
- Copy that must appear verbatim:
  - "Questionnaire Dashboard"
  - "Track and manage all your questionnaires in one place."
  - Status labels: "Completed", "In Progress", "Needs Review", "Draft"
  - Sample rows: "NovaTech Solutions", "Stride Labs" (used in the search scene)
  - "New Questionnaire"

## Creative Direction
- Tone preset: default
- Creative direction: calm control center for questionnaire chaos — clean, confident, quietly satisfying
- Interpretation: motion carries the energy (snappy filter/re-sort, beat-locked reorder); typography stays clean and restrained; no jokes at the product's expense
- Angle: A wall of questionnaires in mixed states gets tamed live on screen — search narrows it, a column-header click re-sorts it, the badge/avatar system explains itself at a glance. The video's job is to make "messy list → understood" feel satisfying.
- Hook: Hard cut straight into the full, busy table (7 rows, 4 status colors, avatars) with the line "7 questionnaires. 4 companies waiting on you."
- Outro / punchline: "Questionnaire Dashboard — every questionnaire, one screen, zero guessing," with a confident highlight pulse on "New Questionnaire."
- Avoid:
  - Generic SaaS language ("streamline your workflow," etc.)
  - Abstract filler visuals — every scene must show the real table/UI
  - Unrelated visual redesign — keep the exact Tailwind palette and component structure from the source file

## Visual Identity
- Background: #F9FAFB page / #FFFFFF card & table
- Text: #111827 headings / #6B7280 secondary text
- Accent: #2563EB (primary button, focus ring)
- Status colors: emerald #059669 (Completed), blue #2563EB (In Progress), amber #D97706 (Needs Review), gray #6B7280 (Draft) — each as a soft pill background + colored dot, matching the source component's `STATUS_STYLES` / `STATUS_DOT` maps
- Assignee avatar colors: reuse the source component's per-row pastel combos (e.g. orange-200/orange-800, indigo-200/indigo-800, purple-200/purple-800, pink-200/pink-800)
- Display/body font: system sans-serif (Tailwind default stack, Inter-like — -apple-system, Segoe UI, Roboto)
- Visual references from the project: the `STATUS_STYLES`, `STATUS_DOT`, and `ICON_BG` color maps and the exact row/column layout from `QuestionnaireDashboard.tsx`

## Storyboard
Use the storyboard in `brag-output/brag-plan.md` as the creative contract.

Scene summary:
1. Cold open — 0-3s — full busy table + hook line "7 questionnaires. 4 companies waiting on you."
2. Search narrows it — 3-8s — type "Stride" into search, table live-filters to the one matching row
3. Status + assignee language — 8-13s — status badges then avatar chips arrive one by one (beat-grid: 8.52s, 9.52s, 10.52s, 11.52s, 12.52s)
4. Sort snaps it into order — 13-18s — click "Last Updated" header, all 7 rows reorder in one pass, beat-locked to 17.02s (strong cue)
5. Outro — 18-21s — "New Questionnaire" button click-pulse beat-locked to 20.02s, closing line, music fades

## Audio
- Audio role: warm, light corporate bed under sparse, motion-matched UI SFX
- Audio arc: low under the cold open, builds through search and the badge/avatar sequence, peaks at the sort-reorder payoff (16-18.5s strong-cue cluster), fades out under the outro line
- Music: `happy-beats-business-moves-vol-1-by-ende-dot-app.mp3` (copied into `assets/music/`)
- Music treatment: fade in under Scene 1, steady rise through Scenes 2-3, full presence through Scene 4's beat-locked reorder, fade out across Scene 5
- Music cue guidance: cue source is `<hyperframes-skill-dir>/assets/music/cues/happy-beats-business-moves-vol-1-by-ende-dot-app.music-cues.json` (bundled preset, 120 BPM). Strong cues used: 17.02s (Scene 4 reorder, beat-locked) and 20.02s (Scene 5 button click, beat-locked). Beat grid (~0.5s spacing) used for Scene 3's sequential badge/avatar reveal, snapped to every other beat (~1s per item) per the reading-time floor.
- Audio-reactive treatment: planned as subtle (table-card shadow/presence breathing with music RMS during Scene 1), but skipped in this build per the audio-reactive fallback rule — the RMS-extraction helper workflow was out of scope for this pass and skipping it does not block the render or the creative laws. Documented here rather than faked with a non-audio-driven tween.
- Audio-coupled moments:
  - Scene 1 — headline typed with subtle key ticks
  - Scene 2 — search-input typing sound; soft card-drop as non-matching rows fade out
  - Scene 3 — soft sequential tick per badge/avatar arrival, one per beat-grid timestamp
  - Scene 4 — one card-slide/whoosh SFX exactly on the 17.02s beat-locked reorder
  - Scene 5 — one soft confirmation tick on the button press at 20.02s
- SFX selection guidance: prefer clean, professional UI sounds — keyboard/interface clicks for typing, a card-slide/switch sound for the reorder, a soft interface tick for the button confirmation. Sparse: no more than ~5 discrete SFX hits total across the video.
- SFX analysis guidance: use `<brag-skill-dir>/assets/sfx/sfx-analysis.md` (and the `interface/`, `keyboard/`, and `casino`/card-slide-style folders under `assets/sfx/`) for candidate files; prefer lower high-frequency-risk sounds since several moments repeat.
- Exact SFX choice: Hyperframes should choose exact filenames, timestamps, density, and volume based on the implemented animation.
- Audio files: copy the chosen music and any Hyperframes-selected SFX into `brag-output/composition/assets/`

## Hyperframes Instructions
Load the composition-building Hyperframes domain skills — `hyperframes-core` (composition contract + `data-*` timing), `hyperframes-animation` (motion), `hyperframes-creative` (design spec, beats, audio-reactive), `hyperframes-keyframes` (seek-safe keyframes), and `hyperframes-cli` (lint/check/render). `/brag` is its own workflow: do not enter the `hyperframes` entry-point intent interview and do not route into its generic promo/launch-video workflow. Prefer native Hyperframes conventions over anything in `/brag`.

Requirements:
- Show at least one real UI, copy, or visual element from the source project (the dashboard table itself, in every scene).
- Keep all text readable in the final render (respect the reading-time floor from the plan).
- Keep the video within 15-25 seconds (target 21s).
- Include the planned music/SFX layer unless a real blocker is documented.
- Treat `/brag` audio notes as guidance, not a fixed cue sheet. Choose exact SFX after the visual animation exists.
- Treat music cue metadata as optional timing hints; ignore cues that hurt readability, scene pacing, or the product story.
- Major reveals may move toward nearby strong cues within about 0.15s. Smaller entrances may align to nearby beat points within about 0.10s. Use only the 2 strong-cue locks named above (17.02s, 20.02s) unless the edit clearly benefits from more.
- Use SFX to support motion and interaction: card sounds for the row reorder, key/click sounds for typing, restraint elsewhere.
- Honor the planned music fade-in/fade-out and the energy build toward the 16-18.5s payoff.
- When wiring the subtle audio-reactive treatment, follow the current `hyperframes-creative` audio-reactive workflow to extract audio data; if extraction is unavailable, document it and skip audio-reactive rather than blocking the render.
- Use local assets for audio and any required runtime/media dependencies.
- Run `hyperframes check` before render — it is brag's single gate.

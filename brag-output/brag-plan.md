# Brag Plan: Questionnaire Dashboard

## What is this app?
A dashboard that tracks every security/compliance questionnaire a team is working on — who owns it, what state it's in, and when it last moved — in one searchable, sortable table.

## The angle
This isn't a mockup of a "workflow tool." It's the actual moment of control: a wall of questionnaires in different states of chaos (Draft, Needs Review, In Progress, Completed) gets tamed by one search box and one click on a column header. The video's job is to make that moment — messy list → sorted, filtered, understood — feel satisfying.

## Hook (first 2-3 seconds)
Hard cut into the dashboard already full of rows — seven questionnaires, four different status colors, avatars everywhere. Before any explanation: "7 questionnaires. 4 companies waiting on you." Immediate, a little overwhelming, on purpose.

## Key moments (the middle)
- Cursor clicks into the search box and types "Stride" — the table narrows live to the one matching row, the "Needs Review" amber badge sitting front and center.
- Cursor clicks the "Last Updated" column header — the whole table re-sorts, rows sliding into new positions in one smooth pass.
- A close-in on the status badges themselves: emerald "Completed" dot, blue "In Progress" dot, amber "Needs Review" dot, gray "Draft" dot — the color language of the whole product in one glance.
- The assignee avatars (RV, NI, AM, DP...) land as a row of colored initials — "everyone's accountable, everyone's visible."

## Outro / punchline
The "New Questionnaire" button gets a single confident click-highlight. Final card: "Questionnaire Dashboard — every questionnaire, one screen, zero guessing."

## User flow worth showing
1. Entry: dashboard loads with the full table — 7 questionnaires, mixed statuses, avatars, search bar and "New Questionnaire" / "Share" actions in the header.
2. Key action: type "Stride" into the search box (live filter), then click the "Last Updated" column header (live re-sort).
3. Result: the table lands filtered/sorted — the exact row the user needed, front and center, badge and assignee clearly legible.

## Tone
- Preset: default
- Creative direction: calm control center for questionnaire chaos — clean, confident, a little satisfying (the "everything clicks into place" feeling)
- Interpretation: playful but not silly; motion carries the energy (snappy re-sorts, live filtering) while typography stays clean and the product itself does the talking. No jokes at the product's expense — the humor, if any, is in how much calmer the "after" feels than the "before."

## Format: landscape — 1920x1080
## Duration: 21 seconds

## Visual identity (from the project)
- Background: #F9FAFB (Tailwind gray-50, page) / #FFFFFF (card/table)
- Accent: #2563EB (Tailwind blue-600, primary button + focus ring)
- Text: #111827 (gray-900, headings) / #6B7280 (gray-500, secondary text)
- Status colors: emerald-600 (#059669) Completed, blue-600 (#2563EB) In Progress, amber-600 (#D97706) Needs Review, gray-500 (#6B7280) Draft
- Display font: system sans-serif (Tailwind default stack — Inter-like: -apple-system, Segoe UI, Roboto)
- Body font: same system sans-serif stack, regular weight
- Strongest visual element: the status-badge color system (soft pill backgrounds + colored dot) paired with the colored initials avatars — the product's whole visual language in two repeating UI elements

## Share copy (draft)
Built a Questionnaire Dashboard that actually tells you what's Completed, what Needs Review, and who owns it — search, sort, done.

## Audio direction
- Role: warm, light corporate bed under crisp, sparse UI SFX
- Music: happy-beats-business-moves-vol-1-by-ende-dot-app.mp3 (bundled skill track)
- Music treatment: starts at low volume under the hook, rises slightly into the search/sort sequence, gentle fade under the final card/logo
- Music cue guidance: read from `<skill-dir>/assets/music/cues/happy-beats-business-moves-vol-1-by-ende-dot-app.music-cues.json` (120 BPM). In the 0-25s planning window, strong cues cluster later — 16.02s, 17.02s, 17.52s, 18.02s, 18.52s, 20.02s — because the track's intro/build is calmer and its energy lands after ~16s. Storyboard timing below is shaped around that: the sort-reorder payoff (the single biggest visual beat) lands on the 17.02s strong cue, and the outro button-click lands near 20.02s. The badge/avatar sequential reveal (8-13s) uses the general beat grid (~0.5s apart at 120 BPM) snapped to every other beat (~1s per item) to stay within the reading-time floor.
- Audio-reactive treatment: subtle — table-card shadow/presence may breathe slightly with music RMS during the idle open shot; nothing on text
- SFX posture: sparse, professional — one UI click/type sound for the search interaction, one card-slide/switch sound for the column re-sort, one soft confirmation tick on the final button highlight
- Audio-coupled moments: typing "Stride" (light key ticks), rows re-sorting (a single card-slide whoosh, not per-row), avatar row arriving (soft sequential ticks, held under reading floor)
- Restraint rule: no per-keystroke sound spam while typing, no more than 3 distinct SFX hits total, nothing louder than the music bed

## Storyboard

### Scene 1 — Cold open: the wall of questionnaires — 0.00-3.00s (3s)
Full dashboard table visible immediately: 7 rows, all 4 status colors present, avatars, header with search bar and "New Questionnaire" button. Headline overlay types in: "7 questionnaires. 4 companies waiting on you."
Sequential/interaction: none — full table is already visible; headline text types on character by character
Audio intent: sets the scene, slightly busy/anticipatory
Audio-coupled idea: headline typed with subtle key ticks
Music: bed enters low (intro is calm through ~16s per cue guidance)
Transition mood: clean → Scene 2

### Scene 2 — Search narrows it — 3.00-8.00s (5s)
Cursor clicks the search input, types "Stride" letter by letter; table rows filter live down to the single "Stride Labs" row with its amber "Needs Review" badge.
Sequential/interaction: yes — search box fills character by character, table rows drop out one by one as filter narrows (fast, ~0.15s apart, non-text motion)
Audio intent: focus, satisfaction of narrowing down
Audio-coupled idea: type sound on search input; soft card-drop sound as non-matching rows fade out
Music: bed continues, still building
Transition mood: clean → Scene 3

### Scene 3 — The language of status + who owns it — 8.00-13.00s (5s)
Search clears. Close-in crop on 3-4 status badges (Completed / In Progress / Needs Review / Draft) landing one by one, followed immediately by 3-4 assignee avatar chips (RV, NI, AM, DP) landing one by one alongside them.
Sequential/interaction: yes — badges then avatars arrive one by one, each held ~0.9-1.0s // beat-grid: badge 1 at 8.52s, badge 2 at 9.52s, badge 3 at 10.52s, avatar 1 at 11.52s, avatar 2 at 12.52s (every-other beat from the ~0.5s grid, so text stays readable)
Audio intent: rhythmic, builds anticipation toward the payoff
Audio-coupled idea: soft sequential tick per badge/avatar arrival, motion-matched to each beat-grid timestamp above
Music: still building toward the drop
Transition mood: quick zoom out to full table → Scene 4

### Scene 4 — Sort snaps it into order — 13.00-18.00s (5s)
Full 7-row table visible again. Cursor clicks the "Last Updated" column header; rows animate into newly sorted positions in one smooth ~0.6s reorder pass, newest at top. // beat-locked: 17.02s (strong_beat, 1.00)
Sequential/interaction: yes — all 7 rows reposition together in a single beat-locked reorder motion, not per-row
Audio intent: the payoff — the "click" moment, biggest hit of the video
Audio-coupled idea: one satisfying card-slide/whoosh SFX timed to land exactly on the 17.02s reorder
Music: strong-cue cluster (16.02-18.52s) — the track's energy peak
Transition mood: dramatic (quick zoom on the header) → Scene 5

### Scene 5 — Outro / punchline — 18.00-21.00s (3s)
Cut to "New Questionnaire" button getting a single confident highlight/click pulse. // beat-locked: 20.02s (strong_beat, 1.00). Card resolves to: "Questionnaire Dashboard — every questionnaire, one screen, zero guessing."
Sequential/interaction: yes — one simulated click on "New Questionnaire," timed to the 20.02s beat
Audio intent: confident close
Audio-coupled idea: one soft confirmation tick on the button press, landing on 20.02s; music fades under final line
Music: fades out over the scene
Transition mood: soft hold → end

**Music mood for this video:** upbeat, light corporate, quietly confident
**Audio summary:** A warm business-pop bed rises gently from the cold open through the search-and-sort payoff, carries three sparse motion-matched SFX (type, card-slide, confirmation tick), and fades out under the closing line — never louder or busier than the UI it's supporting.

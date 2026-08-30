# E·Δelta — TrackShift 2026 Presentation Site

An animated, self-contained presentation website for **E-Delta** (TrackShift 2026 · AI
Motorsport Intelligence · PS1: Energy & Overtake Intelligence), built to be screen-recorded
as the video submission.

Everything is a single file — `index.html`. No build step, no internet, no dependencies.

## Run it

```bash
# either just open the file in Chrome/Edge (double-click), or serve it:
python3 -m http.server 8000
# → http://localhost:8000
```

Press `F11` for full screen before recording.

## 🎬 Autopilot mode (recommended for recording)

Click **"▶ AUTOPILOT PRESENTATION"** on the cover (or press `A`) and the entire
presentation runs itself: slides advance on cue, an animated cursor moves and clicks
everything, the live demo plays through both decision points, on-screen captions follow
the narration, and the narration is **spoken aloud** through your browser's speech engine.
You only need to start your screen recorder and press the button. `Esc` stops it.

Voice quality depends on the browser:

- **Microsoft Edge** → best result (it exposes the "…Natural" neural voices — sounds
  genuinely human). Record in Edge if you can.
- **Chrome** → decent ("Google US English"; needs internet for the good voice).
- Prefer your own voice? Mute the tab/system audio, run autopilot, and speak over it —
  the captions double as your teleprompter.

Recording checklist: full screen (`F11`), start OBS/QuickTime, park your real mouse in a
corner (the page hides it during autopilot), click the button, don't touch anything until
the closing slide. Total runtime ≈ 5 minutes.

## Controls

| Key / control | Action |
|---|---|
| `↓` / `↑` (or `PageDown`/`PageUp`) | Next / previous section |
| `Space` | Play / pause the live demo (section 06 only) |
| Right-side dots | Jump to any section |
| Demo buttons | `PLAY`, `1×/2×`, jump to `DETECTION` moment, jump to `THE PASS`, restart |

The demo **auto-pauses** at the two decision points (Detection Line approach on lap 7, and
the pre-pass window on lap 8) and shows the counterfactual comparison table. Press `Space`
to continue each time.

## Section map (11 screens)

1. **Cover** — hook + wordmark
2. **The problem** — 2026 step-change stats + the five coupled challenges
3. **Energy Shadow Price** — λE formula, the 0.2 MJ > 0.3 MJ insight
4. **Architecture** — pipeline, stack, planner bounds, Fieni-as-oracle positioning
5. **Rule engine** — YAML, action mask example, ERS-K power-profile chart, boundary tests
6. **Rival belief filter** — four types, Bayes update, Ji/Liu/Tang (2024) anchor
7. **Live demo** — British GP Sprint replay, laps 7–8, HAM vs ANT (simulated twin, labeled)
8. **Evaluation** — acceptance metrics + provenance label legend
9. **Circuit generalization** — six GP buckets, Silverstone vs Spa
10. **Grounded, not hyped** — the six claims we deliberately don't make
11. **The pitch** — closing line

## Suggested 3½-minute recording script

Record at 1920×1080 (or 4K), full screen, cursor hidden where possible. Two rehearsal
runs first — submit a take with zero fumbles.

- **0:00–0:20 · Cover.** "In 2026 Formula 1, the hard question is not how much energy
  remains — it's what the next 0.1 MJ is worth. We built E-Delta to answer that."
- **0:20–0:45 · Problem.** Read the five challenges quickly; land on "this is a partially
  observable sequential decision problem, not a battery gauge."
- **0:45–1:05 · Shadow Price.** "One number changes the question." Explain λE and the
  0.2 MJ > 0.3 MJ threshold insight.
- **1:05–1:25 · Architecture + rules.** "Real replay in, legal recommendation out — and
  illegal actions never even reach the planner." Point at the mask example and the
  345/355 km/h profiles.
- **1:25–1:45 · Rival belief.** "We don't guess the rival, we keep a belief" — four types,
  peer-reviewed Bayesian-game anchor.
- **1:45–3:00 · LIVE DEMO (the centerpiece).** Press PLAY. Narrate the lap-7 auto-pause
  (compare HOLD / ATTACK EARLY / DETECTION_PUSH / FULL ATTACK — "0.74 vs 0.31 detection
  conversion for 0.18 MJ"), resume through the Detection Line toast, then the lap-8 pause
  and the pass at 4.575 km. Say the honesty line out loud: "the real position change
  anchors the scenario — the energy state is a labeled simulation."
- **3:00–3:20 · Evaluation + generalization.** Zero rule violations, calibration,
  sensitivity; six circuit buckets, Silverstone vs Spa.
- **3:20–3:40 · Close.** "F1 teams know how much energy they have. E-Delta tells them
  what the next 0.1 MJ is worth."

## Recording tips

- OBS Studio (free) or QuickTime; capture the browser in full screen, 60 fps if available.
- Record narration as a separate audio track if you can — easier to fix a fumbled line.
- Use `1×` demo speed while talking; `2×` if you're running long.
- The site needs no network — safe to record offline.

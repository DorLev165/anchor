# Anchor

Real-time anxiety self-help app (ages 14+, US). Single self-contained file: `index.html`
(vanilla HTML/CSS/JS, no external resources, all state in localStorage). Deployed via GitHub Pages:
https://dorlev165.github.io/anchor/ — push to `main` and Pages redeploys in ~1 minute.

**`SPEC.md` is the binding product/clinical spec (from the product owner — Dor's aunt).**
Never invent therapeutic content or principles beyond it; if content is missing, ask her (via Dor).
Don't rebuild what works — adapt.

Key internals (`index.html`):
- `SIT` — per-situation content pools (her exact wording; typographic quotes, UTF-8 required).
- `PATHS` / `composePath()` — IDENTIFY answer → tool sequence; intensity ≥8 prepends breathing, trims to one middle tool.
- Control tool samples 3+3 cards per use; wrong sorts get a gentle correction, then auto-place.
- `finishRecord()` → `anchor.sessions2`; step follow-up (20-min gate on `anchor.pending`) drives
  `anchor.pathScores` — taking the step (+3) outweighs anxiety-delta (±2). Success = acted, not calmed.
- Safety: `SAFETY_RE` on all free text → 988 screen, flow stops.
- localStorage: `anchor.profile2`, `anchor.sessions2`, `anchor.pathScores`, `anchor.pending`, `anchor.meta`.
- Theme tokens defined three ways (bare `:root`, `prefers-color-scheme` guard, `[data-theme]`) — keep all in sync.

- `stepsFor(sit, inLoop)` / `LOOP_STEPS` — the small step depends on situation **and** mechanism.
  A loop about health must not be offered social actions; entry points that don't ask the
  situation (JUST HELP ME NOW) use the generic pack rather than guessing one.

`review/index.html` is the public content-review page (every situation × mechanism with verbatim
copy, pools, ladders, shared screens, and a reassurance/avoidance/checking scan) at
https://dorlev165.github.io/anchor/review/ — regenerate it whenever route copy changes.

Verify changes by serving locally (`python3 -m http.server`) and driving flows in a browser
(the top-level `ACTS` / `S` / `go` are reachable from the console).

Hebrew for the product owner: never paste it from the terminal (RTL comes out mirrored) —
write a file and `open -e` it so it can be copied from TextEdit.

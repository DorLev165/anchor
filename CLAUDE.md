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

Verify changes by serving locally (`python3 -m http.server`) and driving flows in a browser
(the top-level `ACTS` / `S` / `go` are reachable from the console).

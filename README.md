# Orca

TradingView Pine Script v6 — team trader **Orca** (BOS / MSS / setup circles / dealing ranges).

Main file: [`Orca.pine`](Orca.pine)

## Visible settings

| Group | Options |
|-------|---------|
| Core | Bars L/R, break type, BOS/MSS colors & width |
| Circles | **Show orange circles**, **Show ONLY setup circles**, sizes/colors |
| Patterns | Bullish/bearish reversal & continuation toggles |
| Dealing Range | Box + **0.5** (and optional 0.618 / 0.786) |

Disabled HTF / label / protected options are hardcoded off and **hidden** from Inputs.

## Behavior

- **Show ONLY setup circles** — hides non-setup marks when on  
- **Show orange circles** — separate toggle for MSS extreme (orange) circles (only when setup-only is off)  
- Dealing range only when **two consecutive circles are the same color** (green→green or red→red)
- **Only the last** dealing range is kept (previous box/levels are removed)

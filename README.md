# Orca HTF Fractals

TradingView Pine Script v6 — **Williams Fractals** (Periods = **3**). **Not date-hardcoded.**

## Markers

- Shape: **circle** (no timeframe text, no emoji)
- Color by **bias**: Uptrend (HH/HL) green · Downtrend (LH/LL) red

## 50% lines (settings group)

Toggle each TF mid independently, each with its own color. Example on **1m**: show 1H + 15m + 5m + 1m 50% lines together.

| Setting | Default color |
|---------|---------------|
| Show 1H 50% | orange |
| Show 15m 50% | cyan |
| Show 5m 50% | yellow |
| Show 1m 50% | magenta |

## Marker timeframe map

| Chart | Shows |
|-------|--------|
| 1H | 1H fractals |
| 15m | **1H** fractals |
| 5m | **15m** fractals |
| 1m | 5m fractals |

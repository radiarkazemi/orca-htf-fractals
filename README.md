# Orca HTF Fractals

TradingView Pine Script v6 — **Williams Fractals** (Periods = **3**). **Not date-hardcoded.**

## Markers

- Shape: **circle** (no `1H H` / `5m L` text)
- Color by **bias**:
  - **Uptrend** (higher high / higher low) → green
  - **Downtrend** (lower high / lower low) → red

## Test anchors (1H, NY)

| Side | Candle |
|------|--------|
| High | Fri **31 Jul 2026 02:00** |
| Low  | Fri **31 Jul 2026 10:00** |
| High | Wed **5 Aug 2026 03:00** |
| Low  | Wed **5 Aug 2026 06:00** |

## Timeframe map

| Chart | Shows |
|-------|--------|
| 1H | 1H fractals |
| 15m | **1H** fractals |
| 5m | **15m** fractals |
| 1m | 5m fractals |

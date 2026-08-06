# Orca HTF Fractals

TradingView Pine Script v6 — **Williams Fractals** (same as built-in Fractals). **Not date-hardcoded.**

## Periods

Use **Periods = 3** (matches your Fractals chart). Periods=2 is noisier.

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

## Logic

`ta.pivothigh` / `ta.pivotlow` with Left = Right = **Periods** (default 3).

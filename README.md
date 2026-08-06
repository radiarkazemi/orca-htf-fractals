# Orca HTF Fractals

TradingView Pine Script v6 — **Williams Fractals** (same logic as the built-in Fractals indicator). **Not date-hardcoded.**

## Test anchors (1H, NY)

| Side | Candle | Fractal |
|------|--------|---------|
| High | Wed **5 Aug 2026 03:00** | Up fractal (green/teal ▲) |
| Low  | Wed **5 Aug 2026 06:00** | Down fractal (red ▼) |

Also valid Williams fractals: Fri 31 Jul 2026 **02:00** high / **10:00** low.

## Timeframe map

| Chart | Shows |
|-------|--------|
| 1H | 1H fractals |
| 15m | **1H** fractals |
| 5m | **15m** fractals |
| 1m | 5m fractals |

## Logic

1. `ta.pivothigh` / `ta.pivotlow` with Left/Right periods (default **2/2**, same as TradingView Fractals)
2. Up fractal = local high → teal ▲ above the candle
3. Down fractal = local low → red ▼ below the candle
4. Confirmed `right` bars after the pivot (no lookahead)

## Settings

- **Fractal Left / Right** = 2 / 2
- **Min swing (× ATR)** = **0** (mark every fractal like the Fractals indicator; raise to hide tiny swings)
- **Keep last N** = 50 (or 0 = all)

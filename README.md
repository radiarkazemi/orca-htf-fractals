# Orca HTF Fractals

TradingView Pine Script v6 indicator for multi-timeframe **dealing-range** highs/lows.

## What it marks

Alternating market-structure swings built from fractal pivots:

1. Fractal pivot high/low (default left=2, right=2) = candidate
2. Swings must alternate H ↔ L
3. Same direction updates if more extreme (so a weak 05:00 low yields to the real 10:00 low)
4. Optional minimum leg size (× ATR) before accepting the opposite swing

### 1H anchor (America/New_York)

| Side | Candle | Role |
|------|--------|------|
| High | Fri 31 Jul 2026 **02:00** | dealing-range high |
| Low  | Fri 31 Jul 2026 **10:00** | dealing-range low |

On GC=F that pair is roughly **4145 H / 4076 L** (spot XAU brokers differ in absolute price; the candle times are the pattern).

## Timeframe map

| Chart | Shows |
|-------|--------|
| 1H | 1H MS swings (local) |
| 15m | 1H swings |
| 5m | 15m swings |
| 1m | 5m swings |

## How to use

1. Open [`Orca_HTF_Fractals.pine`](./Orca_HTF_Fractals.pine)
2. Copy all
3. TradingView → Pine Editor → Paste → Save → Add to chart
4. Start on **1H**, NY timezone, and confirm markers on Fri 02:00 high + Fri 10:00 low
5. Drop to 15m / 5m / 1m — same HTF swings should project down

## Style

- High = red triangle
- Low = green triangle
- Optional 😊 emoji, H/L tags, 50% midline
- `Show ONLY latest High + latest Low` keeps just the active dealing-range pair

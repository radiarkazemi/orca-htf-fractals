# Orca HTF Fractals

TradingView Pine Script v6 indicator for multi-timeframe dealing-range highs/lows.

## Timeframe map
| Chart | Shows |
|-------|--------|
| 1H | 1H swing @ MSS (local) |
| 15m | 1H signals |
| 5m | 15m signals |
| 1m | 5m signals |

## How to use
1. Open [`Orca_HTF_Fractals.pine`](./Orca_HTF_Fractals.pine)
2. Copy all
3. TradingView → Pine Editor → Paste → Save → Add to chart
4. Start on **1H** to verify markers (~4088 high / ~4022 low style)

## Logic
On MSS, marks the **latest swing** (`lastSH` / `lastSL`), not the absolute extreme since BOS.
- High = red
- Low = green
- Optional 50% midline + emoji markers

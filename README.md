# Orca HTF Fractals

TradingView Pine Script v6 dealing-range highs/lows. **Not date-hardcoded.**

## Test anchor (NY time)

| Side | Candle |
|------|--------|
| High | Fri 31 Jul 2026 **02:00** area |
| Low  | Fri 31 Jul 2026 **10:00** |

## Timeframe map

| Chart | Shows |
|-------|--------|
| 1H | 1H dealing ranges |
| 15m | **1H** dealing ranges |
| 5m | **15m** dealing ranges |
| 1m | 5m dealing ranges |

So on **5m** you should see a **15m H** near the Fri 02:00/02:15 high (same selloff that 1H marks at 02:00).

## Logic

1. Major ZigZag leg (`Major leg × ATR`)
2. Opposite DR side = highest high / lowest low in the last `DR window (hours)` from the leg extreme (default 8h) — so 15m does not stick a tiny 09:15 LH over 02:15
3. If a bullish leg is invalidated by a new LL, flip bearish and keep the prior high (keeps 02:15 → 10:00 on 15m)
4. Completed legs are stored in history; live leg updates too

## Settings

- **Show ONLY latest…** = off (to see history)
- **DR window (hours)** = 8
- **Major leg (× ATR)** = 3 (lower = more marks)

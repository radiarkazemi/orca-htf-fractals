# Orca HTF Fractals

TradingView Pine Script v6 indicator for multi-timeframe **dealing-range** highs/lows.

Nothing is date-hardcoded. Fri 31 Jul 2026 02:00 / 10:00 is only a test anchor.

## Logic

1. Detect a major ZigZag leg when the move is at least `Major leg × ATR`
2. Bearish leg → mark last **internal lower-high before the low** + the **leg low**
3. Bullish leg → mirror (internal higher-low + leg high)
4. When the leg reverses, that pair is **saved into history**
5. The active (in-progress) leg also shows a live pair

## Settings that matter

| Input | Default | Effect |
|-------|---------|--------|
| Major leg (× ATR) | 3.0 | Lower = more marks, higher = fewer |
| Show ONLY latest High + latest Low | **false** | Must be off to see history |
| Show live dealing range | true | Marks the current unfinished leg |
| Keep last N | 12 | History depth |

## Timeframe map

| Chart | Shows |
|-------|--------|
| 1H | 1H dealing ranges |
| 15m | 1H dealing ranges |
| 5m | 15m dealing ranges |
| 1m | 5m dealing ranges |

## How to use

1. Copy [`Orca_HTF_Fractals.pine`](./Orca_HTF_Fractals.pine) into TradingView Pine Editor
2. Add to chart (timezone America/New_York)
3. Confirm Fri 02:00 H + Fri 10:00 L **and** earlier legs are also marked
4. Tune **Major leg (× ATR)** if you want denser or cleaner marks

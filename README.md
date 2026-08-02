# Orca HTF Fractals

TradingView Pine Script v6 indicator for multi-timeframe **dealing-range** highs/lows.

## Anchor pattern (America/New_York)

| Side | Candle | FxPro XAU ≈ |
|------|--------|-------------|
| High | Fri 31 Jul 2026 **02:00** | ~4088 |
| Low  | Fri 31 Jul 2026 **10:00** | ~4022 |

`02:00` is a **lower high** after the Jul 30 peak. Older HH/MS logic kept the peak and skipped it.

## Logic

1. Build a major ZigZag leg (`Major leg × ATR`, default 3.0)
2. On a bearish leg, mark:
   - last **internal** fractal lower-high **before** the leg low → `02:00`
   - the leg low → `10:00`
3. Bounce highs after the low (e.g. Fri 15:00) are ignored
4. Default **Show ONLY latest High + latest Low** → one clean dealing-range pair

## Timeframe map

| Chart | Shows |
|-------|--------|
| 1H | 1H dealing range |
| 15m | 1H dealing range |
| 5m | 15m dealing range |
| 1m | 5m dealing range |

## How to use

1. Copy [`Orca_HTF_Fractals.pine`](./Orca_HTF_Fractals.pine)
2. TradingView → Pine Editor → Paste → Save → Add to chart
3. Chart timezone **UTC-4 / America/New_York**
4. On **1H**, confirm 😊 on Fri 02:00 high and Fri 10:00 low
5. If too quiet/noisy, adjust **Major leg (× ATR)** (try 2.5–4.0)

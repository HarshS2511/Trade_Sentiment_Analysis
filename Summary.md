# Trader Performance vs Market Sentiment — Project Summary

---

## Methodology

- Loaded and merged two datasets: **211,224 trader transactions** + **2,644 daily sentiment records**
- Aligned both datasets on date (daily level), simplified sentiment into **Fear / Neutral / Greed**
- Created daily per-account metrics: PnL, win rate, trade frequency, position size, L/S ratio
- Performed sentiment analysis, trader segmentation, and built a predictive model

---

## Key Insights

|   | Insight |
|---|---------|
| 1 | **Fear days generate higher average PnL** ($5,185) vs Greed days ($4,144) — traders profit more during market fear by buying dips aggressively |
| 2 | **Traders use larger positions on Fear days** ($8,530 avg) and are more long-biased (2.45x L/S ratio vs 1.76x on Greed days) |
| 3 | **PnL is more volatile on Fear days** — bigger winners AND bigger losers |
| 4 | **High Frequency traders earn 3x more** than Low Frequency traders |
| 5 | **Large traders consistently outperform** small traders across all sentiment conditions |

---

## Strategy Recommendations

### Rule 1 — Fear Days: Go Long, Go Big
> During Fear days, large-capital traders should **increase long exposure** —
> dip-buying during fear periods shows consistent outperformance.

### Rule 2 — Greed Days: Trade Less, Trade Smarter
> During Greed days, **reduce trade frequency** and focus on high-conviction
> setups only — fewer but better trades win during bullish sentiment.

---

## Predictive Model Results

| Property | Value |
|---|---|
| **Model** | Logistic Regression |
| **Accuracy** | 90% |

### Most Predictive Features (in order)

1. **win_rate** - strongest predictor of profitability
2. **sentiment_enc** - market sentiment significantly impacts outcomes
3. **ls_ratio** - long/short bias predicts direction of profit

---

*Submitted for: Data Science / Analytics Intern Role — Primetrade.ai*

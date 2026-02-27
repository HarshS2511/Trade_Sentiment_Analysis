# Trade_Sentiment_Analysis
# Trader Performance vs Market Sentiment


## Objective
Analyze how Bitcoin market sentiment (Fear/Greed Index) relates to trader behavior and performance on Hyperliquid, and uncover patterns that could inform smarter trading strategies.

---

## Project Structure
```
├── Trader_Sentiment_Analysis.ipynb   ← Main analysis notebook
├── fear_greed.csv                     ← Bitcoin Fear/Greed Index dataset
├── trader_data.csv                    ← Hyperliquid trader transactions
├── charts/                            ← All generated charts
│   ├── chart1_performance_by_sentiment.png
│   ├── chart2_behavior_by_sentiment.png
│   ├── chart3_pnl_distribution.png
│   ├── chart4_segments.png
│   ├── chart5_pnl_over_time.png
│   └── chart6_model_feature_importance.png
└── README.md
```

---

## Setup & How to Run

### Requirements
```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

### Run the Notebook
```bash
jupyter notebook Trader_Sentiment_Analysis.ipynb
```
Run all cells top to bottom. Charts will be saved to the `charts/` folder automatically.

---

## Datasets
| Dataset | Rows | Columns | Date Range |
|---------|------|---------|------------|
| Fear/Greed Index | 2,644 | 4 | 2018–2025 |
| Trader Data | 211,224 | 16 | May 2023–May 2025 |
| **Merged** | **211,218** | **20** | **May 2023–May 2025** |

---

## Key Insights

### Insight 1 — Fear Days = Higher (but Volatile) PnL
Average daily PnL is **$5,185 on Fear days vs $4,144 on Greed days**. However, Fear days show wider dispersion extreme winners pull the mean up while many traders lose. Median PnL is actually higher on Greed days ($265 vs $123), showing more consistent returns.

### Insight 2 — Traders Go Bigger & Longer During Fear
On Fear days, average position size is **$8,530 vs $5,955** on Greed days. Long/Short ratio is **2.45x during Fear vs 1.76x during Greed** traders aggressively buy dips, and it pays off when markets rebound.

### Insight 3 — High Frequency & Large Traders Win More
- High Frequency traders earn **3x more** ($10,713 avg PnL) than Low Frequency ($3,541)
- Large Traders earn **$9,324 avg PnL** vs $4,930 for Small Traders
- But Low Frequency traders have **higher win rates** (1.45 vs 1.16), suggesting consistency vs volume tradeoff

---

## Strategy Recommendations

### Rule 1: "Fear = Opportunity for Large, Long-Biased Traders"
> During Fear days, high-capital accounts (avg size >$10K) should **increase long exposure**. The market overreacts to fear dip-buying strategies consistently outperform during these periods.

### Rule 2: "Greed Days = Trade Less, Trade Smarter"
> During Greed days, **reduce trade frequency** and focus on high-conviction setups only. Data shows fewer trades with better selectivity yields more consistent profits during bullish sentiment.

---

## Bonus — Predictive Model
A **Logistic Regression** model trained on behavioral features (trade frequency, position size, win rate, long/short ratio, sentiment) achieves **90% accuracy** in predicting whether a trader will be profitable on a given day. Win rate and L/S ratio are the strongest predictors.

---

*Submitted by: Harsh*

*Role: Data Science / Analytics Intern*

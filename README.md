# PrimeTrade Sentiment & Trader Analysis

## Overview
This project analyzes Bitcoin market sentiment using the Fear/Greed index and historical Hyperliquid trade records. It produces a reproducible Python notebook with data cleaning, feature engineering, analytical visualizations, trader segmentation, and a bonus profitability model.

## Files
- `PrimeTrade_analysis.ipynb` — main notebook with the full analysis and visualizations.
- `fear_greed_index.csv` — Bitcoin sentiment dataset.
- `historical_data.csv` — Hyperliquid trade dataset.

## Setup Instructions
1. Install required Python packages:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
2. Open `PrimeTrade_analysis.ipynb` in Jupyter or VS Code Notebook.
3. Run the notebook cells sequentially.

## How to Run
- If using Jupyter Lab / Notebook:
  ```bash
  jupyter lab
  ```
- If using VS Code, open the notebook and run the cells from top to bottom.

## Summary of Results
- **Sentiment impact:** Fear periods show the highest trading volume but lower win rates compared to Greed periods.
- **Risk exposure:** Average trade exposure is highest during Fear and Extreme Greed, suggesting elevated risk at sentiment extremes.
- **Directional bias:** Long vs short trade share stays roughly balanced across sentiment states.
- **Trader segments:** The notebook segments traders into high/low exposure, frequent/infrequent, and consistent/inconsistent groups based on PnL variance and trade counts.
- **Actionable recommendations:** Reduce exposure during Fear, apply sentiment-aware trade sizing, and monitor high-variance accounts more closely.

## Notes
- The dataset does not include a direct leverage field, so the notebook uses `Size USD` as a proxy for trade exposure.
- The analysis is intentionally conservative and highlights edge cases such as sentiment periods not covered by the trades dataset.

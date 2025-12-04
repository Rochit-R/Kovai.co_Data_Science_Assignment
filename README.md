# Kovai.co_Data_Science_Assignment
Forecasting public transport ridership using SARIMA, Prophet, and ensemble models with human-insight-driven workflow and visualizations.


# Public Transport Ridership Forecasting — Key Insights Report

> **Name:** Rochit R  
> **Reg No:** 727822TUAM045  
> **Department:** AIML  
> **College:** Sri Krishna College of Technology  
> **Date:** 04-12-2025  

---

## Insight 1 — Initial Exploration & Observations
While exploring the dataset, I noticed daily ridership data for six transport services over five years. Rapid Route and Peak Service had high variability, whereas School and Local Route were more stable. Missing values were minimal, mostly in the "Other" category, which I interpolated. Examining summary statistics revealed occasional extreme spikes. This step highlighted the **importance of cleaning and understanding trends before modeling** for forecast accuracy.

## Insight 2 — EDA & Pattern Recognition
During exploratory data analysis:
- Weekly seasonality: commuter-heavy services peak on weekdays; school services fluctuate less.
- Rolling averages (7-day and 30-day) smoothed daily noise and revealed trends.
- Correlation heatmaps showed interdependent services, e.g., Local Route correlates with Peak Service (~0.75).

This stage helped **formulate modeling strategies**, realizing that simple models wouldn’t capture seasonal or correlated patterns.

## Insight 3 — Modeling Strategy & Feature Engineering
Implemented a layered approach:
1. **Naive and Moving Average** models — baseline trends.  
2. **SARIMA** — captures trend, seasonality, and autocorrelation.  
3. **Prophet** — includes external regressors like weekends and day-of-week.  
4. **Ensemble** — weighted combination using inverse-RMSE.

Added **lag features (1,7,30 days) and rolling means** to improve performance and interpretability, bridging raw observations into actionable forecasts.

## Insight 4 — Fine-Tuning & Learning
- SARIMA required careful selection of (p,d,q)(P,D,Q,s) parameters.  
- Prophet regressors reduced prediction error.  
- Ensemble weighting balanced strengths of each model.  

This iterative tuning gave deeper insight into trade-offs and improved forecast reliability while keeping human interpretability.

## Insight 5 — Model Evaluation & Decision
Models were compared using RMSE, MAE, and MAPE:
- Naive: simple but misses seasonality.
- MA7: captures short-term trends effectively.
- SARIMA and Prophet: capture seasonality and external factors.
- Ensemble: balanced, robust forecasts, ideal for planners.


## Final Takeaways & Learnings
Combining statistical and ML approaches improves forecasting:
- SARIMA provides mathematically grounded predictions.  
- Prophet allows human-interpretable regressors.  
- Ensemble integrates multiple insights for robustness.  

EDA, feature engineering, and iterative tuning are essential to generate meaningful forecasts. Visualizations further enhance human comprehension, making this workflow practical for real-world transport planning.

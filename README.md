# Bitcoin Market Activity and Internet Attention

**EDAB6808 · Assignment 1 · University of the Free State**

## Project overview

This project investigates whether internet search attention leads or follows Bitcoin returns, trading volume and volatility. It combines time-series analysis, machine learning and volatility modelling to assess whether observed statistical relationships also improve forecasts on unseen data.

The central question is whether Google Trends provides useful information about Bitcoin market behaviour during 2025.

## Data and scope

- Bitcoin market series covering prices, returns, trading volume and volatility.
- Google Trends search-interest measures for Bitcoin-related keywords.
- A 2025 study period, with the report interpreting the lead–lag results at weekly horizons.

## Analytical approach

1. Prepare and align the market and search-attention series.
2. Examine stationarity using Augmented Dickey–Fuller tests.
3. Explore timing relationships through cross-correlation.
4. Use Granger tests to assess predictive precedence.
5. Compare Random Forest forecasts with benchmark predictions.
6. Examine volatility using market inputs, attention inputs and GARCH modelling.

## Key findings

- General Bitcoin search attention showed its strongest predictive relationship with trading volume at a two-week lag, with a Granger-test p-value of approximately **1.41 × 10⁻⁸**.
- Some return relationships were statistically significant, but the Random Forest return model did not outperform the mean benchmark on the test set.
- Adding search-attention variables did not improve the reported market-only volatility forecast.

| Test comparison | Model | Benchmark or alternative |
| --- | --- | --- |
| Bitcoin return RMSE | Random Forest: **0.0565** | Mean benchmark: **0.0522** |
| Volatility RMSE | Market plus attention: **0.0178** | Market only: **0.0168** |

Lower RMSE indicates smaller prediction errors. The findings suggest that search attention was more informative about market participation than reliable return prediction in this sample.

## Repository materials

| Material | Contents |
| --- | --- |
| Jupyter notebook (`.ipynb`) | Data preparation, statistical tests, model comparisons, visualisations and saved analysis outputs. |
| Executive report (`.pdf`) | Research question, methods, findings, interpretation and limitations. |

## Tools and skills

Python, pandas, NumPy, matplotlib, seaborn, statsmodels, scikit-learn and GARCH modelling. The project develops time-series preparation, statistical testing, benchmark evaluation and financial interpretation.

## Interpretation and limitations

Granger causality indicates predictive precedence under the tested specification; it does not establish economic causation. Significant timing relationships did not consistently translate into better forecasts. Results depend on the study period, aggregation, keyword selection and evaluation split, and do not establish a profitable trading strategy.

## Credits

Collaborative coursework by **Lwazi Nhlapo and Reatile Seekoei** for EDAB6808 at the University of the Free State. The accompanying report provides the supporting references and full analytical discussion.

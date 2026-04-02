# High-Dimensional GDP Growth Forecasting with Lasso and Ridge Regularization

## Objective
Forecast cross-country GDP per capita growth using high-dimensional World Development Indicators data, while diagnosing OLS overfitting and applying regularization techniques to improve out-of-sample predictive performance.

## Methodology
- Collected 36 macroeconomic, financial, demographic, and institutional indicators from the World Bank’s World Development Indicators (WDI) via the :contentReference[oaicite:0]{index=0} for ~150 countries (2013–2019), then constructed a cross-sectional dataset using 5-year averages.
- Cleaned the dataset by applying missingness thresholds and imputing remaining values using cross-country medians to preserve sample size.
- Standardized predictors and split the data into training and test sets to evaluate generalization.
- Estimated a baseline :contentReference[oaicite:1]{index=1} model to demonstrate overfitting in a high p/n setting.
- Implemented :contentReference[oaicite:2]{index=2} and :contentReference[oaicite:3]{index=3} using cross-validated λ selection (via :contentReference[oaicite:4]{index=4}) to control variance and improve predictive stability.
- Visualized coefficient shrinkage and variable selection using the Lasso path to analyze how predictors enter the model as regularization weakens.

## Key Findings
- OLS exhibited classic high-dimensional overfitting, achieving near-perfect training fit but substantially weaker test performance, consistent with variance inflation at elevated predictor-to-sample ratios.
- Both Ridge and Lasso regularization reduced the train–test performance gap, improving out-of-sample R² and stabilizing coefficient estimates.
- Lasso produced a sparse model, selecting a small subset of robust predictors from a large correlated feature set, highlighting key drivers of cross-country growth.
- The Lasso Path revealed that the most stable growth indicators enter the model earliest, indicating strong conditional associations that persist even when controlling for a broad set of correlated covariates.

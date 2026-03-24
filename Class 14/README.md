# AI Capex Diagnostic Modeling

## Objective
To rigorously evaluate the statistical integrity of an OLS regression model forecasting AI software revenue by diagnosing heteroscedasticity and multicollinearity, and correcting inferential bias using HC3 robust standard errors.

---

## Methodology
- Constructed an Ordinary Least Squares (OLS) regression model to estimate AI software revenue as a function of capital expenditure and deployment metrics.  
- Performed residual diagnostics to assess model assumptions, with a focus on variance stability across fitted values.  
- Identified heteroscedasticity through visual inspection of residual dispersion patterns at increasing capital expenditure levels.  
- Quantified multicollinearity using the Variance Inflation Factor (VIF) analysis to detect redundant explanatory variables.  
- Re-estimated the model using HC3 heteroscedasticity-consistent covariance estimators to correct biased standard errors.  
- Compared naive and robust model outputs to evaluate the impact on statistical inference and coefficient significance.  

---

## Key Findings
The analysis revealed a pronounced heteroscedastic structure, with residual variance increasing systematically at higher levels of AI capital expenditure. This violation of OLS assumptions resulted in artificially deflated standard errors and overstated statistical significance in the naive model. After applying HC3 robust estimators, standard errors widened appropriately, leading to a more conservative and accurate assessment of predictor significance. Notably, several deployment-related variables previously deemed significant were no longer statistically robust, underscoring the critical importance of correcting for heteroscedasticity in high-variance, capital-intensive AI markets.

---

## Tech Stack
- Python  
- pandas  
- statsmodels  
- matplotlib  
- seaborn  

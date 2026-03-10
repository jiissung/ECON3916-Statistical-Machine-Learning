# Project Description: Detecting Spurious Correlation in Macroeconomic Data

This project analyzes macroeconomic time-series data from the **Federal Reserve Economic Data (FRED)** database to demonstrate the risks of **spurious correlation** and **multicollinearity** when working with trending economic variables. Using **Python**, I collected key indicators—including inflation (CPI), unemployment, the federal funds rate, industrial production, and the money supply—and constructed a unified dataset for empirical analysis.

## Methodology

### 1. Exploratory Correlation Analysis
I first examined **raw level data** using **pandas** and **seaborn** to generate correlation heatmaps. Because many macroeconomic variables exhibit long-run upward trends, these visualizations revealed artificially high correlations—illustrating the classic **“correlation trap”** in time-series analysis.

### 2. Multicollinearity Diagnostics
To quantify redundancy among predictors, I applied **Variance Inflation Factor (VIF)** diagnostics using **statsmodels**, which highlighted severe **multicollinearity** in the raw dataset.

### 3. Time-Series Transformation
To address these issues, I transformed the non-stationary variables into **Year-over-Year (YoY) growth rates**, reducing trend-driven correlations and producing more economically meaningful relationships.

### 4. Causal Structure Mapping
Finally, I used **Directed Acyclic Graphs (DAGs)** to conceptually map the underlying structural relationships between macroeconomic variables, distinguishing **causal pathways** from misleading statistical associations.

## Key Insight

This workflow demonstrates a practical methodology for **identifying and correcting spurious relationships in macroeconomic time-series data**, combining statistical diagnostics, data transformations, and **causal reasoning** to produce more reliable empirical insights.

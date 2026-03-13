# Data Wrangling & Engineering Pipeline

## Objective
Develop a robust preprocessing pipeline to transform a structurally messy HR economics dataset into a modeling-ready format by diagnosing missingness mechanisms, engineering categorical features, and resolving econometric identification risks.

## Methodology

- **Data Ingestion & Audit**
  - Imported the dataset `messy_hr_economics.csv` using Python and conducted an initial structural audit using `pandas`.
  - Evaluated column types, summary statistics, and missing-value distributions to understand the data-generating environment.

- **Missing Data Diagnostics**
  - Used the `missingno` library to visually inspect missingness patterns through matrix visualizations.
  - Identified structural alignment of missing values across variables, indicating a **Missing At Random (MAR)** mechanism rather than purely random missingness.

- **Conditional Imputation Strategy**
  - Applied **conditional median imputation** where missing numeric variables were filled based on group-level medians of relevant conditioning variables.
  - This preserved cross-sectional structure in the data while minimizing bias introduced by naive global imputation.

- **Categorical Feature Engineering**
  - Encoded categorical predictors for regression modeling.
  - Avoided the **Dummy Variable Trap** by dropping a reference category to prevent perfect multicollinearity within the design matrix.

- **High-Cardinality Compression**
  - Applied **Target Encoding** to compress high-cardinality geographic variables (e.g., state-level indicators).
  - This reduced dimensionality while preserving predictive signal for downstream econometric modeling.

- **Econometric Model Preparation**
  - Constructed a regression-ready feature matrix suitable for use with `statsmodels`.
  - Ensured that the design matrix satisfied identification requirements and avoided linear dependency among regressors.

## Key Findings

The analysis revealed that missing data in the dataset followed a **structured MAR pattern**, rather than purely random absence, allowing for principled conditional imputation. By implementing a disciplined feature engineering strategy—including reference-class encoding and target encoding for geographic variables—the final dataset avoided multicollinearity and excessive dimensionality. The resulting pipeline produced a clean, econometrically sound feature matrix ready for regression analysis and further causal investigation.

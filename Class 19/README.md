# Tree-Based Models — Random Forests

## Objective
Evaluate and compare the predictive performance of tree-based and linear models on housing price data, and demonstrate how ensemble methods improve generalization in non-linear settings.

## Methodology
- Analyzed the California Housing dataset (20,640 observations, 8 features)
- Trained and evaluated Decision Tree, Ridge Regression, and Random Forest models
- Assessed model performance using RMSE and R² on both training and test sets
- Tuned Random Forest hyperparameters using GridSearchCV (n_estimators, max_depth, max_features)
- Compared feature importance using Mean Decrease in Impurity (MDI) and permutation importance
- Converted the regression problem into a classification task (predicting above-median prices)
- Evaluated classification performance using AUC, comparing Random Forest and Logistic Regression
- Built an interactive dashboard using Plotly and ipywidgets to visualize model performance, feature importance, and parameter sensitivity

## Key Findings
- Random Forest significantly outperformed linear and single-tree models, achieving **Test R² ≈ 0.809**, compared to Ridge Regression (**≈ 0.576**) and Decision Tree (**≈ 0.622**)
- Hyperparameter tuning provided modest but measurable improvements, indicating the default Random Forest was already near-optimal
- Random Forest classifier achieved **AUC ≈ 0.961**, outperforming Logistic Regression (**≈ 0.906**), highlighting the importance of modeling non-linear relationships
- Feature importance analysis showed **median income (MedInc)** as the dominant predictor, with location variables (latitude, longitude) also contributing meaningfully
- The interactive dashboard demonstrated diminishing returns from increasing the number of trees and illustrated how model performance and feature importance shift with hyperparameter choices

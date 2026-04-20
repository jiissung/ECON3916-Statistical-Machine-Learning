## Causal ML — Double Machine Learning for 401(k) Policy Evaluation

### Objective  
Estimate the causal impact of 401(k) eligibility on household net financial assets using modern Double Machine Learning techniques that account for high-dimensional confounding and nonlinear relationships.

---

### Methodology  
- Simulated a data-generating process (DGP) to demonstrate **regularization bias**, showing that naïve LASSO underestimates the true treatment effect (TRUE_ATE = 5.0) by shrinking coefficients toward zero.  
- Implemented a **DoubleML Partially Linear Regression (PLR)** framework to obtain debiased causal estimates.  
- Used **Random Forest models** as flexible nuisance learners for both outcome and treatment equations.  
- Applied **5-fold cross-fitting** to reduce overfitting and ensure orthogonalization of residuals.  
- Estimated the **Average Treatment Effect (ATE)** of 401(k) eligibility on net financial assets using U.S. pension data.  
- Conducted **Conditional Average Treatment Effect (CATE)** analysis by income quartiles to explore heterogeneity.  
- Visualized subgroup treatment effects with **confidence intervals** to assess statistical significance across income levels.  

---

### Key Findings  
- Naïve regularization methods (LASSO) introduce **substantial bias** in causal settings, reinforcing the need for orthogonalized estimation approaches like DoubleML.  
- The estimated ATE indicates that 401(k) eligibility **increases net financial assets by approximately _[INSERT ATE VALUE]_**, suggesting a meaningful positive effect on household wealth accumulation.  
- CATE analysis reveals **heterogeneous treatment effects across income groups**:  
  - Lower-income households exhibit **smaller or less precise gains**, potentially due to limited capacity to contribute.  
  - Middle-income households show **moderate positive effects**, reflecting partial uptake and savings behavior.  
  - Higher-income households experience the **largest gains**, consistent with greater participation rates and contribution levels.  
- Overall, the results suggest that while 401(k) eligibility is beneficial on average, its impact is **unevenly distributed**, with stronger effects concentrated among higher-income groups.  

---

This project demonstrates how modern causal machine learning methods can uncover both average policy effects and meaningful heterogeneity that would be obscured under traditional estimation approaches.

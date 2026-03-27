# 📊 The Polynomial Trap: Bias-Variance Tradeoff

## 📌 Overview
This project investigates the **bias-variance tradeoff** through controlled experiments on both synthetic and real-world datasets. The objective is to demonstrate how model complexity affects generalization performance and to apply reliable model selection techniques.

---

## 🎯 Objectives
- Visualize overfitting and underfitting using polynomial regression  
- Analyze **complexity curves** (training vs. test error)  
- Apply **K-fold cross-validation** for model selection  
- Compare high-dimensional vs. parsimonious models on real data  

---

## 🛠️ Tools & Technologies
- Python  
- NumPy  
- scikit-learn (`PolynomialFeatures`, `LinearRegression`, `cross_val_score`)  
- Matplotlib  

---

## 📂 Datasets
### Synthetic Data
- Generated from: `y = sin(2πx) + noise`  
- 50 training observations  
- 200 test observations  

### Ames Housing Dataset
- 1,460 observations  
- 80 features  

---

## 🔍 Methodology
- Fit polynomial regression models across degrees 1–15  
- Construct **complexity curves** comparing training vs. test RMSE  
- Use **K-fold cross-validation** to estimate out-of-sample performance  
- Perform feature selection using correlation analysis  

---

## 📈 Key Findings
1. Polynomial degrees **3–5** provided optimal performance on synthetic data  
2. **Cross-validation-selected models matched true test-optimal models**, validating CV as a reliable selection method  
3. On housing data, a **5-feature model outperformed the kitchen-sink model** in CV RMSE despite having lower training R²  

---

## 🧠 Key Takeaways
- Increasing model complexity reduces bias but increases variance  
- **Cross-validation is essential** for selecting models that generalize well  
- Simpler models can outperform complex ones on unseen data  
- Feature selection improves performance in high-dimensional settings  

---

## 🚀 Impact
This project highlights practical skills in:
- Model evaluation and diagnostics  
- Bias-variance analysis  
- Cross-validation and generalization assessment  
- Translating technical results into actionable insights 

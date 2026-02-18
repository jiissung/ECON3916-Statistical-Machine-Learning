# Hypothesis Testing & Causal Evidence Architecture  
**Project:** *The Epistemology of Falsification — Hypothesis Testing on the Lalonde Dataset*

---

## Objective  

Most data projects stop at *estimation* — calculating an effect and reporting a coefficient.  
In this lab, I pivoted to **falsification**.

Using the Lalonde (1986) experimental dataset, I operationalized the scientific method to adjudicate between competing narratives of causality:

- **Narrative A:** Job training increases post-program earnings  
- **Narrative B (Null Hypothesis):** Observed differences are random noise  

Rather than asking *“What is the effect?”* I asked:

> “Can we statistically reject the possibility that this effect is noise?”

This reframes the task from prediction to **epistemic validation**.

---

## Technical Approach  

To construct a defensible evidence architecture, I implemented both parametric and non-parametric hypothesis tests using SciPy’s statistical framework.

### 1️⃣ Parametric Signal Detection (Welch’s T-Test)  
- Estimated the Average Treatment Effect (ATE) via difference in means.  
- Used Welch’s T-Test to account for unequal variances between treatment and control groups.  
- Interpreted the T-statistic as a **Signal-to-Noise ratio**.  
- Controlled for **Type I error (α = 0.05)** to maintain inferential discipline.  

### 2️⃣ Non-Parametric Validation (Permutation Test — 10,000 Resamples)  
- Constructed an empirical null distribution by randomly permuting treatment labels.  
- Tested whether the observed earnings lift could plausibly emerge under random assignment.  
- Avoided distributional assumptions (earnings data are heavy-tailed and non-normal).  
- Cross-validated the parametric p-value against the permutation-derived p-value.  

This dual-layer testing strategy ensured that statistical significance was not an artifact of asymptotic assumptions.

---

## Key Findings  

- Estimated treatment effect: **~$1,795 increase in real earnings (re78)**  
- Both Welch’s T-Test and the Permutation Test rejected the Null Hypothesis  
- Statistical significance was robust across parametric and empirical null frameworks  

**Conclusion:**  
The observed earnings lift is unlikely to be due to chance — evidence supports a causal impact of job training in the experimental setting.

This constitutes **proof by statistical contradiction**: assuming no effect leads to improbably extreme observed outcomes.

---

## Business Insight  

Rigorous hypothesis testing functions as the **Safety Valve of the Algorithmic Economy**.

In production environments, unchecked estimation leads to:

- Data dredging  
- P-hacking  
- Spurious correlations  
- Overfit narratives dressed as causal claims  

By embedding falsification logic into the workflow:

- We prevent false discoveries (Type I errors)  
- We distinguish signal from volatility  
- We protect decision systems from statistical illusion  

In high-stakes environments — growth optimization, policy evaluation, pricing algorithms — hypothesis testing is not academic ceremony. It is governance infrastructure.

Robust statistical contradiction testing ensures that deployed insights are not artifacts of randomness, but defensible causal evidence.

---

## Takeaway  

This lab demonstrates that causal inference is not merely about computing effects — it is about **engineering doubt** into the system and allowing evidence to survive adversarial scrutiny.  

Estimation produces numbers.  
Falsification produces knowledge.

Return-Aware Experimentation at Netflix reframes A/B testing around expected business impact rather than arbitrary statistical thresholds. Instead of treating p < 0.05 as the decision rule, experiments are evaluated based on expected return — weighing effect size, uncertainty, user impact, and implementation cost. In academia, 0.05 controls Type I error as a scientific convention; in industry, decision thresholds are optimized for risk-adjusted value. In other words, statistical significance informs the decision, but business return determines it.

# Recovering Experimental Truths via Propensity Score Matching

## Objective
To demonstrate how econometric techniques can correct selection bias in observational data and recover the true causal treatment effect when randomized control is absent.

## Overview
Observational studies often produce misleading treatment estimates due to non-random selection into treatment. In this project, I analyzed the observational subset of the Lalonde dataset to replicate a classic causal inference failure and systematically correct it using Propensity Score Matching (PSM). The objective was to recover the experimentally validated treatment effect from biased non-experimental data.

## Methodology

- **Modeled Selection Bias:** Estimated treatment assignment probabilities using logistic regression to capture systematic differences between treated and control groups.  
- **Estimated Propensity Scores:** Generated individual-level probabilities of treatment conditional on covariates using Python, Pandas, and Scikit-Learn.  
- **Applied Nearest-Neighbor Matching:** Matched treated observations to observationally similar controls based on propensity score proximity to construct a balanced comparison group.  
- **Re-estimated Treatment Effect:** Computed post-matching outcome differences to approximate the experimental benchmark.

## Key Findings

- The naïve observational estimate produced a severely biased treatment effect of **–$15,204**, driven by non-random selection.  
- After implementing Propensity Score Matching, the corrected estimate recovered the true experimental effect of approximately **+$1,800**.  
- The analysis demonstrates how explicitly modeling the selection mechanism restores causal credibility in observational research.

## Technical Stack

- Python  
- Pandas  
- Scikit-Learn  
- Logistic Regression Modeling  
- Nearest-Neighbor Matching  

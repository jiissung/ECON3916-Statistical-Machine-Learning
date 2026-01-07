Here’s a polished, analyst‑grade README.md entry you can drop directly into your project:

Global Purchasing Power Parity Analysis
Objective
This project evaluates the validity of the Law of One Price by comparing international Big Mac prices and assessing whether currency valuations align with their implied purchasing power parity (PPP) levels.
Methodology
- Ingested raw 2015 Big Mac Index data by manually constructing a structured dataset using Python dictionaries.
- Standardized the data in Pandas to compute each country’s implied PPP exchange rate relative to the U.S. dollar.
- Calculated the percentage overvaluation or undervaluation of each currency by comparing market exchange rates to their PPP-implied benchmarks.
- Interpreted deviations as indicators of potential mispricing, inefficiencies, or arbitrage opportunities in global currency markets.
Key Findings
Based on the computed implied PPP values and valuation differentials, the analysis revealed meaningful departures from parity across several currencies. For example:
Overall, the results highlight how real‑world frictions—such as transportation costs, market segmentation, and pricing power—can cause persistent deviations from the theoretical equilibrium implied by the Law of One Price.

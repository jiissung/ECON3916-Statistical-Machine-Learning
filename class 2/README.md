The Illusion of Growth & The Composition Effect
Objective

This project investigates long-run U.S. wage dynamics by constructing a Python-based data pipeline that ingests live macroeconomic data from the Federal Reserve Economic Data (FRED) API. The goal is to evaluate whether apparent wage growth reflects genuine increases in purchasing power or is distorted by inflation and statistical composition effects—particularly during economic shocks such as the COVID-19 pandemic.

Methodology

Using Python and the fredapi, I built a reproducible workflow to fetch, transform, and visualize official economic time series:

Nominal vs. Real Wages

Retrieved nominal average hourly earnings data (AHETPI) from FRED.

Retrieved Consumer Price Index (CPI) data to deflate nominal wages and compute real wages.

Constructed long-run time-series visualizations to compare nominal wage growth against real purchasing power.

Anomaly Detection: The 2020 Pandemic Spike

Identified a sharp increase in measured real wages during 2020.

Hypothesized that this spike reflected a composition effect rather than genuine wage pressure.

Composition Effect Correction

Fetched the Employment Cost Index (ECIWAG), a wage measure designed to hold workforce composition constant.

Rebased both wage measures to a common index to enable direct comparison.

Demonstrated that while standard averages showed a sudden spike, the ECI exhibited smooth, stable growth—confirming the anomaly was statistical rather than economic.

Key Findings

The Money Illusion: Despite substantial nominal wage growth since the 1960s, real wages have remained largely flat once inflation is accounted for, illustrating the persistent gap between perceived and actual economic progress.

The Pandemic Paradox: The apparent wage boom in 2020 was not driven by rising labor demand or improved compensation, but by the disproportionate exit of low-wage workers from employment. This mechanically increased average wages while leaving underlying wage structures unchanged.

Statistical Insight: By contrasting standard wage averages with the Employment Cost Index, the project highlights how improper aggregation can produce misleading economic narratives during periods of labor market disruption.

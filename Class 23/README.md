## FedSpeak Analysis — NLP on FOMC Minutes

### Objective
To quantitatively analyze the evolution of Federal Reserve communication by applying natural language processing techniques to FOMC meeting minutes, with the goal of identifying shifts in sentiment, uncertainty, and underlying policy language regimes over time.

### Methodology
- Collected and preprocessed FOMC meeting minutes, including tokenization, lemmatization, and removal of stop words to standardize textual inputs  
- Constructed a TF-IDF document-term matrix using both unigrams and bigrams to capture key economic phrases and contextual meaning  
- Computed Loughran-McDonald sentiment metrics, including net sentiment (positive minus negative word share) and uncertainty (frequency of uncertainty-related terms)  
- Visualized sentiment and uncertainty trends over a 20+ year period, incorporating rolling averages and macroeconomic event annotations  
- Reduced dimensionality of the TF-IDF matrix using PCA (via TruncatedSVD) and applied K-Means clustering to identify distinct communication regimes  
- Compared sentiment distributions across pre-COVID and post-COVID periods to assess structural changes in Federal Reserve tone  

### Key Findings
The analysis reveals three distinct language regimes in FOMC communication, broadly corresponding to pre-crisis stability, crisis-era response (including the Global Financial Crisis and COVID shock), and the post-pandemic tightening environment. Clustering results indicate that crisis periods are characterized by more homogeneous language centered on risk, stabilization, and policy intervention, while non-crisis periods exhibit more varied and growth-oriented communication.

Sentiment analysis shows a clear structural shift following March 2020, with net sentiment declining and uncertainty rising relative to the pre-COVID period. This reflects the heightened economic volatility and policy ambiguity introduced by the pandemic, as well as the Federal Reserve’s increased emphasis on risk management. While sentiment partially recovers in the post-2021 period, uncertainty remains elevated, suggesting a more cautious and data-dependent communication strategy in the current policy regime.

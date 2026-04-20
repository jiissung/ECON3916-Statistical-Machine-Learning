## Clustering World Economies with K-Means & PCA

### Objective
To identify latent economic groupings across countries and regions by applying unsupervised learning techniques to development indicators, and to evaluate how closely these data-driven clusters align with established income classifications.

### Methodology
- Collected 10 World Bank development indicators for approximately 160 countries using wbgapi  
- Standardized all features using StandardScaler to ensure comparability across variables with different scales  
- Applied K-Means clustering with an initial specification of K = 4 to partition countries into homogeneous groups  
- Evaluated cluster structure across K = 2 to K = 10 using the elbow method and silhouette scores to determine the optimal number of clusters  
- Reduced dimensionality using Principal Component Analysis (PCA) and visualized clusters in a 2D feature space  
- Cross-tabulated resulting clusters against World Bank income classifications (low, lower-middle, upper-middle, high income) to assess economic interpretability  
- Replicated the full pipeline on the California Housing dataset to test whether similar clustering structure emerges at a subnational level  

### Key Findings
The analysis identified an optimal clustering structure at K = 4, consistent with the elbow inflection point and peak silhouette performance, suggesting a stable partition of global economies. The resulting clusters exhibited strong alignment with World Bank income groupings, particularly at the extremes: high-income and low-income countries were largely well-separated, indicating that the selected indicators capture meaningful differences in economic development. However, overlap between lower-middle and upper-middle income groups revealed transitional economies where development characteristics are less distinct.

At the subnational level, applying the same methodology to California census tracts produced economically interpretable clusters, broadly distinguishing high-income urban areas, lower-income inland regions, and mixed suburban zones. This reinforces the broader finding that K-Means, when paired with appropriate scaling and dimensionality reduction, can uncover coherent socioeconomic structures across both global and regional datasets.

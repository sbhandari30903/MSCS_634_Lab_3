# MSCS_634_Lab_3
# Clustering Analysis Using K-Means and K-Medoids Algorithms
# Clustering Analysis Lab

## Purpose
This lab explores the application of two popular clustering techniques—K-Means and K-Medoids—on the Wine dataset from `sklearn`. By standardizing the features, fitting each algorithm with \(k=3\), and evaluating with Silhouette Score and Adjusted Rand Index (ARI), the goal is to understand how cluster definitions differ and when one method may be preferable over the other.

## Key Insights
- **Performance Metrics**: Both algorithms produced reasonable clusters, but K-Medoids showed slightly higher robustness to outliers, reflected in a marginally better Silhouette Score in our experiments. ARI values for both methods confirmed that clusters aligned closely with the true varietal labels.
- **Cluster Shapes**: 2D PCA visualizations revealed that K-Means centroids sometimes fell between natural groupings, whereas K-Medoids medoids (actual data points) captured representative samples more faithfully.
- **Algorithmic Trade-offs**:
  - *K-Means* is computationally efficient and well-suited to spherical, homogeneous clusters. Its centroids can, however, be skewed by extreme values.
  - *K-Medoids* (PAM implementation) is more robust to noise and uses actual observations as centers, but at a higher runtime cost, making it better for smaller datasets or situations with outliers.

## Challenges and Decisions
- **Package Installation**: K-Medoids requires the `scikit-learn-extra` extension, which added a dependency step to the workflow.
- **Visualization**: Reducing high-dimensional data to 2D via PCA was chosen for clarity, though different feature combinations could yield alternative cluster interpretations.
- **Parameter Choice**: The number of clusters was fixed at \(k=3\) based on known class labels; in other settings, one would need to use methods like the Elbow Method or Gap Statistic to select \(k\).


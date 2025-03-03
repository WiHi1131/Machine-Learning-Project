<a href = "https://wihi1131.github.io/Machine-Learning-Project/">Home</a>

# Comparison of Clustering Algorithms

Many types of clustering algorithms are available within Python's sklearn library. Below is a comparison of three types of clustering algorithms: K-means, Hierarchical clustering, and DBSCAN (density) clustering: 

- K-Means: The basic idea of K-Means is that is partitions given data into k clusters, where k is defined by the user before the algorithm begins. It iterates through a dataset, assigning points to the closest cluster centroid (a measure of the "center" of a cluster of points), and then updates all centroid locations after adding new data. K-Means is relatively fast, and easy to interpret. However, the user must choose k clusters without necessarily knowing the optimal number of clusters, which can lead to misleading results if a suboptimal k is chosen. Clusters are also assumed to be convex in shape - clusters of data that are not convex in shape or are of varying density may cause this algorithm to struggle. K-Means is also sensitive to outliers, as clusters may be pulled by extreme values.
- Hierarchical Clustering: This is a type of clustering algorithm that constructs clusters by conglomerating or dividing in a nested manner. Specifically, the commonly used AgglomerativeClustering from Python's sklearn utilizes a "bottom-up" approach, where each data point begins as a separate cluster, and then clusters are aggregated to each other in each step of the algorithm. The merging process can be visualized by a tree or dendrogram. As opposed to K-Means, this clustering method can be done without using random initial points, as every point in the dataset starts as its own cluster and clusters are formed by iteratively merging clusters together. Users of this algorithm can also specify the distance metrics to be used in calculating how far apart clusters are. This method is excellent for capturing hierarchical relationships between clusters, and it can accomodate more flexible cluster shapes than K-Means. However, it can also be more computationally expensive, is less suitable for very large datasets due to memory and/or time constraints, and also requires an input for the desired number of clusters (just like K-Means) or a distance threshold before beginning the algorithm; again, this can lead to suboptimal results if poor values are chosen. 
- DBSCAN (density) Clustering: This algorithm looks at density of points within a dataset and uses this information to determine clusters. It looks for points that are packed together within a certain distance (defined as the eps parameter) and groups them into neighborhoods - points with sufficient neighbors become core points that expand into clusters, and any points unreachable by these neighborhoods are defined as outliers or noise. Unlike the first two algorithms, this does not require specifying the number of clusters beforehand, as the number of clusters in the dataset are discovered through density metrics. This makes this algorithm extremely useful for finding unusually shaped clusters. However, selecting correct parameters for 'eps' and the minimum number of samples for a cluster can be challenging, this algorithm may not perform well if the dataset has highly varied density between clusters, and this algorithm also can perform poorly on large data or data with high dimensionality. 

# Data Prep

## Before Cleaning

For our clustering algorithms, we will use the same dataset that was used for <a href = "https://wihi1131.github.io/Machine-Learning-Project/PCA">PCA</a>. Below is a snippet of this dataset: 

<div>
  <img src = "images/pre_pca_data.PNG" title = "Pre-Clustering Data" alt = "Pre-Clustering Data">
  <div>
    <p>
      <b>This is the data that clustering will be performed on, before cleaning. Note that the "label" in this case would be placement. Note also the many quantitative features. Time measurements (game length and time eliminated) are in seconds. Link to data: <a href = "https://github.com/WiHi1131/Machine-Learning-Project/blob/main/data/PRE_PCA.csv">Pre-Clustering Data</a></b>
    </p>
  </div>
</div>

## After Cleaning

<div>
  <img src = "images/PCA_clean.PNG" title = "Cleaned Clustering Data" alt = "Cleaned Clustering Data">
  <div>
    <p>
      <b>This is the data that clustering will be performed on, after cleaning. Note that the "placement" column has been removed, and both non-quantitative columns have also been removed. Link to data: <a href = "https://github.com/WiHi1131/Machine-Learning-Project/blob/main/data/PCA.csv">Cleaned Clustering Data</a></b>
    </p>
  </div>
</div>



<a href = "https://wihi1131.github.io/Machine-Learning-Project/">Home</a>

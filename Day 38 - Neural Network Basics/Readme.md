# Day 37: K-Means Clustering - Grouping Data Points Intelligently

## Overview
This notebook focuses on the **K-Means Clustering** algorithm, an unsupervised machine learning method used for partitioning data into distinct groups or clusters based on similarity. K-Means aims to minimize intra-cluster variance and maximize inter-cluster variance, effectively grouping similar data points together.

In this task, we will implement K-Means clustering on the **Boston Housing Dataset**, working with selected features to demonstrate how the algorithm works in practice.

## Key Concepts

- **Clustering**: A type of unsupervised learning where the goal is to group similar data points together.
- **K-Means Algorithm**: Partitions the data into \(k\) clusters, each represented by the mean of the points in that cluster. The algorithm iteratively assigns points to clusters and updates cluster centers to minimize within-cluster variance.
- **Centroid**: The center of a cluster.
  
## Dataset
The Boston Housing Dataset is used in this notebook. However, only three columns (features) are selected for simplicity and visualization. You can replace this dataset with your own to explore K-Means clustering on different data.

## Prerequisites
Before running this notebook, ensure you have the following packages installed:

```bash
pip install pandas numpy scikit-learn matplotlib
```

## Instructions for Use
1. **Load the Dataset**: Load the dataset, and preprocess it by selecting the relevant columns for clustering.
2. **Standardize the Data**: Use `StandardScaler` to normalize the features, ensuring the clustering is not biased by differing feature scales.
3. **Apply K-Means Clustering**: 
    - Select the number of clusters \(k\).
    - Fit the K-Means algorithm to the data.
    - Analyze the results by inspecting the cluster centers and assigned labels.
4. **Evaluate the Model**: Use metrics such as inertia to determine how well the data points are clustered. Visualize the clustering result using a scatter plot.
5. **Adjust \(k\) Value**: Experiment with different values of \(k\) to find the optimal number of clusters using the Elbow Method.

## Files
- `K-Mean_Clustering.ipynb`: The main notebook implementing the K-Means clustering algorithm on the Boston Housing dataset.

## Results
By the end of this notebook, you should:
- Understand how the K-Means algorithm works.
- Be able to apply K-Means clustering to any dataset.
- Know how to evaluate clustering performance and adjust the number of clusters effectively.

## Conclusion
K-Means clustering is a simple yet powerful algorithm for identifying groupings in your data. This notebook demonstrates how to use it to partition data into meaningful clusters, which can be applied in various domains such as market segmentation, image compression, and anomaly detection.
# CryptoClustering
## Unsupervised_Learning

### Introduction

In this challenge, I will use my knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. This analysis aims to cluster cryptocurrencies based on their market performance using K-means clustering.

### Project Structure

1. Data preprocessing:
    The cryptocurrency market dataset was loaded and examined.
    Summary statistics and initial plots are generated to understand the data.
   
2. Data normalization:
    Use the `StandardScaler()` module from `scikit-learn` to normalize the data.
    Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

3. Find the Best Value for k Using the Original Scaled DataFrame
    The elbow method is used on the original scaled data to find the optimal number of clusters `k`.

4. Cluster Cryptocurrencies with K-means Using the Original Scaled Data
    K-means clustering is applied using the optimal k found.
    The clusters are visualised using hvPlot.

5. Optimise Clusters with Principal Component Analysis
    Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
    Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

6. Find the Best Value for k Using the PCA Data
    The elbow method is used on the original scaled data to find the optimal number of clusters `k`.

7. Cluster Cryptocurrencies with K-means Using the PCA Data
    K-means clustering is applied using the optimal `k` on the PCA data.
    The clusters are visualised using hvPlot.

8. Comparison of Results:
    Composite plots are created to contrast the elbow curves and clustering results.
    The impact of using fewer features for clustering is analysed.

### Results

1. Original Data Clustering:
    Clusters formed with some overlaps in certain plots.
    Optimal k identified using the elbow method.

2. PCA Data Clustering:
    Clearer and more distinct clusters with reduced overlaps.
    Optimal k identified using the elbow method.

3. Same Number of Clusters:
    Both methods (original scaled data and PCA data) determined the same number of clusters: 4.

### Conclusion

Using PCA for dimensionality reduction before clustering with K-means results in clearer and more distinct clusters. This approach reduces the complexity of the data, making clustering more efficient and visualisation more interpretable. However, some information loss may occur due to dimensionality reduction.

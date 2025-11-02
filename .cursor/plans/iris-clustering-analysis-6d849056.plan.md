<!-- 6d849056-d2ea-41a5-89c9-208f1948ee1c c98f2f69-3fbe-4a9d-b0f2-aaa6ade743ac -->
# Iris Dataset Clustering Analysis

## Overview

Create a professional clustering analysis notebook that removes the Species column, performs unsupervised clustering, and compares results with actual species labels.

## Implementation Steps

### 1. Data Loading & Initial Exploration

- Load Iris dataset from `/Users/hariprasad/Repositories/Learning Repositories/nagendra/2_ML_Files/2_Clustering/iris_archive/Iris.csv`
- Display basic info: shape, data types, statistical summary
- Check for missing values and duplicates
- Drop the `Id` column (not useful for clustering)

### 2. Exploratory Data Analysis (EDA)

- **Univariate Analysis**: Distribution plots (histograms/KDE) for all 4 features
- **Bivariate Analysis**: 
- Pairplot/scatter matrix to visualize feature relationships
- Correlation heatmap
- Box plots to identify outliers
- Store Species column separately for later comparison, then remove it from features

### 3. Data Preprocessing

- **Outlier Detection**: Use IQR method or Z-score visualization
- **Feature Scaling**: Apply StandardScaler to normalize all features
- Justify why scaling is critical for distance-based clustering

### 4. Optimal Cluster Determination

- **Elbow Method**: Plot inertia/WCSS for k=1 to 10
- **Silhouette Score**: Calculate and plot for k=2 to 10
- **Analysis**: Determine optimal k value (expect k=3 based on species)

### 5. Clustering Implementation

**K-Means Clustering:**

- Apply K-Means with optimal k and k=3
- Visualize clusters using PCA (2D) and 3D scatter plots
- Display cluster centers

**Hierarchical Clustering (Agglomerative):**

- Create dendrogram to visualize hierarchy
- Apply Agglomerative Clustering with k=3
- Use different linkage methods (ward, complete, average)

**DBSCAN:**

- Determine optimal eps using k-distance graph
- Apply DBSCAN clustering
- Handle noise points appropriately

### 6. Cluster Evaluation & Comparison

**Internal Metrics (without labels):**

- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Score

**External Validation (with Species):**

- Confusion matrix comparing clusters vs actual species
- Adjusted Rand Index (ARI)
- Normalized Mutual Information (NMI)
- Homogeneity, Completeness, V-measure scores

**Visualization:**

- Side-by-side comparison: clustered labels vs actual species
- Cluster distribution analysis
- Misclassification analysis

### 7. Results Summary

- Table comparing all algorithms performance
- Key insights and recommendations
- Discussion on which algorithm best recovered the species structure

## Key Files

- **Input**: `/Users/hariprasad/Repositories/Learning Repositories/nagendra/2_ML_Files/2_Clustering/iris_archive/Iris.csv`
- **Output**: New notebook in `/Users/hariprasad/Repositories/Learning Repositories/nagendra/`

## Libraries Required

- pandas, numpy, matplotlib, seaborn
- sklearn: KMeans, AgglomerativeClustering, DBSCAN, StandardScaler, PCA
- sklearn.metrics: silhouette_score, confusion_matrix, adjusted_rand_score, etc.
- scipy: dendrogram, linkage

### To-dos

- [ ] Load dataset, perform initial exploration and comprehensive EDA with visualizations
- [ ] Preprocess data: handle outliers, scale features using StandardScaler, separate species column
- [ ] Determine optimal number of clusters using Elbow Method and Silhouette Score analysis
- [ ] Implement K-Means clustering with visualization using PCA
- [ ] Implement Hierarchical/Agglomerative clustering with dendrogram
- [ ] Implement DBSCAN clustering with eps optimization
- [ ] Evaluate all algorithms with internal metrics and compare with species labels using external metrics
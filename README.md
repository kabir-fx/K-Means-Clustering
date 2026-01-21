# K-Means Clustering Analysis

This directory contains an implementation of **K-Means Clustering**, a popular unsupervised learning algorithm used to partition data into $K$ distinct, non-overlapping clusters.

## Dataset Overview

The model uses the `Mall_Customers.csv` dataset, which includes:

- **Features Used**:
  - `Annual Income (k$)`: Annual income of the customer.
  - `Spending Score (1-100)`: Score assigned by the mall based on customer behavior and spending nature.
- **Goal**: Segment customers into groups for targeted marketing and behavioral analysis.

## Implementation Steps

The implementation follows these key steps:

1.  **Data Preprocessing**:
    - Importing libraries (`numpy`, `matplotlib`, `pandas`).
    - Extracting features (Annual Income and Spending Score).
2.  **Finding Optimal Clusters**:
    - Used the **Elbow Method** to find the optimal number of clusters.
    - Calculated **WCSS** (Within-Cluster Sum of Squares) for 1 to 10 clusters.
    - Indicated **5 clusters** as the optimal point where the WCSS decrease levels off.
3.  **Model Training**:
    - Used `sklearn.cluster.KMeans`.
    - Parameters: `n_clusters = 5`, `init = 'k-means++'`, and `random_state = 42`.
    - The `k-means++` initialization is used to avoid the random initialization trap.
4.  **Visualization**:
    - Plotted the 5 clusters with distinct colors.
    - Highlighted the **cluster centers** (centroids) to represent the "average" customer in each segment.

## Results

The K-Means algorithm successfully identified 5 customer segments:

- **Cluster 1**: Mid-income, mid-spending (Standard).
- **Cluster 2**: High-income, high-spending (Target/Careless).
- **Cluster 3**: Low-income, low-spending (Sensible).
- **Cluster 4**: Low-income, high-spending (Careless).
- **Cluster 5**: High-income, low-spending (Sensible).

This segmentation provides actionable insights for mall management to tailor their promotional strategies.

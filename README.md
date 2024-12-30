# Customer Segmentation using Clustering Techniques

This repository contains Jupyter notebooks for performing customer segmentation using **K-Means Clustering** and **Hierarchical Clustering**. Customer segmentation is an essential technique for businesses to group their customers based on similar traits and behaviors, enabling more targeted marketing strategies and improved decision-making.

## Overview

### Objective
The goal is to segment customers based on their **Age**, **Annual Income (k$)**, and **Spending Score (1-100)** into meaningful groups to better understand their behavior and preferences.

### Algorithms Used

1. **K-Means Clustering**:
   - K-Means is a centroid-based clustering algorithm that partitions data into \(k\) clusters by minimizing the variance within each cluster.
   - It works iteratively to assign data points to one of the \(k\) clusters based on the distance to the centroid.
   - Strengths: Efficient and scales well with large datasets.
   - Limitations: Requires specifying the number of clusters in advance.

2. **Hierarchical Clustering**:
   - Agglomerative Hierarchical Clustering builds a tree-like structure (dendrogram) by merging data points or clusters iteratively based on their similarity.
   - We use the complete linkage method, which merges clusters based on the maximum distance between points in the clusters.
   - Strengths: Provides a visual representation of clustering (dendrogram) and does not require predefining the number of clusters.
   - Limitations: Computationally intensive for large datasets.

---

## Contents

1. **K_Means_Clustering.ipynb**:
   - Preprocessing:
     - Handles missing values and duplicate records.
     - Encodes categorical variables and scales features using Min-Max normalization.
   - Uses the **Elbow Method** to determine the optimal number of clusters.
   - Visualizes clusters in both 2D and 3D.
   - Provides insights into customer segments.

2. **Hierarchical_Clustering.ipynb**:
   - Preprocessing steps are similar to the K-Means notebook.
   - Constructs a dendrogram to visualize the hierarchical relationships between data points.
   - Groups customers into clusters using the Euclidean distance metric and complete linkage.
   - Analyzes the relationship between clusters and customer demographics.

---

## Dataset

The dataset `Customer.csv` contains the following columns:

- **CustomerID**: Unique identifier for each customer (dropped for clustering).
- **Gender**: Customer’s gender (Male/Female).
- **Age**: Customer’s age.
- **Annual Income (k$)**: Annual income in thousands of dollars.
- **Spending Score (1-100)**: Spending score assigned to the customer based on their purchasing habits.

---

## Results

- **K-Means Clustering**:
  - Segments customers into 5 clusters (determined using the Elbow Method).
  - Each cluster represents a group of customers with similar spending habits and income levels.

- **Hierarchical Clustering**:
  - Produces a dendrogram to visualize how customers group together at different levels of similarity.
  - Allows flexibility in choosing the number of clusters based on the dendrogram.

Both approaches provide meaningful customer segments that can be analyzed for business insights.

---

## Key Insights
- Customers with high spending scores and high income form a distinct cluster, representing high-value customers.
- Low-income customers tend to form clusters based on spending habits, allowing targeted marketing strategies.
- Hierarchical clustering provides additional insights into relationships between clusters that are not immediately visible in K-Means clustering.


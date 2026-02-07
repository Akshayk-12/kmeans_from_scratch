# Implementing and Evaluating K-Means Clustering from Scratch

## Project Overview
This project implements the K-Means clustering algorithm entirely from scratch using NumPy.
The objective is to understand how K-Means works internally without using high-level
machine learning libraries like `sklearn.cluster.KMeans`.

The implementation is tested on a synthetic dataset, and clustering performance is
evaluated using Inertia (WCSS) and Silhouette Score.

---

## Technologies Used
- Python
- NumPy
- scikit-learn (dataset generation & evaluation)
- Matplotlib

---

## Dataset
A synthetic dataset is generated using `sklearn.datasets.make_blobs` with:
- Samples: 500
- Clusters: 4
- Cluster standard deviation: 1.2

---

## K-Means Algorithm (From Scratch)
Steps followed:
1. Randomly initialize K centroids
2. Assign each point to the nearest centroid (Euclidean distance)
3. Update centroids as the mean of assigned points
4. Repeat until convergence or maximum iterations

---

## Evaluation Metrics
- **Inertia (WCSS)**: Measures within-cluster compactness
- **Silhouette Score**: Measures how well clusters are separated

The model is evaluated for **K = 2 to 6**.

---

## Results & Conclusion
- Inertia decreases as K increases
- Silhouette Score peaks at **K = 4**
- Optimal number of clusters: **K = 4**

This matches the ground truth used during dataset creation.

---

## How to Run
1. Clone the repository
2. Install required libraries
3. Run the Python file

```bash
python k_means_from_scratch.py

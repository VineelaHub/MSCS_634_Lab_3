# MSCS 634 Lab 3 - K-Means and K-Medoids Clustering

## Purpose

This lab explores clustering techniques using the Wine Dataset from the `sklearn` Python library. The objective is to apply and compare K-Means and K-Medoids clustering after standardizing the dataset using z-score normalization.

The lab evaluates both algorithms using:

- Silhouette Score
- Adjusted Rand Index (ARI)
- PCA-based two-dimensional cluster visualizations

## Files

- `MSCS_634_Lab_3_KMeans_KMedoids.ipynb`
- `README.md`
- `requirements.txt`

## Key Insights

K-Means and K-Medoids are both used to group the Wine dataset into three clusters.

The Silhouette Score measures how well-separated and cohesive the clusters are. The Adjusted Rand Index measures how closely the generated clusters agree with the actual Wine class labels.

K-Means uses calculated centroids and is generally faster. K-Medoids uses actual observations as cluster representatives, which can make it more robust to outliers.

## Observations

- Standardization is important because Wine dataset features use different numeric scales.
- PCA is used only for visualization.
- Clustering is performed using all standardized features.
- Cluster label numbers are arbitrary and do not need to match the original class numbers.
- K-Means is generally efficient for compact numeric clusters.
- K-Medoids may be preferable when robustness to outliers is important.

## Challenges and Decisions

The `scikit-learn-extra` package may fail to install with Python 3.14 because it can require Microsoft Visual C++ Build Tools.

This project therefore uses the `kmedoids` package and its FasterPAM implementation instead.

PCA is used to reduce the 13 Wine features to two dimensions for visualization while the actual clustering calculations still use the complete standardized dataset.

## How to Run in VS Code

1. Extract the ZIP file.
2. Open the project folder in VS Code.
3. Open the terminal.
4. Run:

```bash
pip install -r requirements.txt
```

5. Open `MSCS_634_Lab_3_KMeans_KMedoids.ipynb`.
6. Select your Python kernel.
7. Click **Run All**.

## GitHub Submission

Create a public repository named `MSCS_634_Lab_3`, upload all three files, and submit the GitHub repository link.

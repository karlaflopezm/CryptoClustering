## Crypto Clustering Project
Overview
This project performs clustering on cryptocurrency market data using K-Means and Principal Component Analysis (PCA). The goal is to identify patterns in cryptocurrency price changes over different timeframes and analyze the impact of dimensionality reduction on clustering results.

### Instructions
#### 1. Load and Explore Data
Rename Crypto_Clustering_starter_code.ipynb to Crypto_Clustering.ipynb.

Load the dataset crypto_market_data.csv into a Pandas DataFrame.

Generate summary statistics and visualize the data to understand its distribution.

#### 2. Data Preprocessing
Use StandardScaler() from scikit-learn to normalize numerical features.

Create a DataFrame with the scaled data.

Set "coin_id" as the index to maintain cryptocurrency labels.

#### 3. Finding the Optimal Number of Clusters (k) using the Elbow Method
Generate a list of k-values ranging from 1 to 11.

Compute inertia for each k and store the values.

Plot the Elbow Curve to determine the optimal k.

Answer: What is the best k-value for clustering based on the elbow method?

#### 4. Clustering Cryptocurrencies using K-Means
Train a K-Means model using the optimal k on the scaled data.

Predict cluster assignments and add them to a new DataFrame.

Visualize the clusters using hvPlot:

X-axis: "price_change_percentage_24h"

Y-axis: "price_change_percentage_7d"

Color: Cluster labels

Hover: "coin_id"

#### 5. Dimensionality Reduction with PCA
Reduce the dataset to three principal components using PCA.

Calculate the explained variance of the three components.

Answer: What percentage of variance is explained by the three principal components?

Create a new DataFrame using the PCA-transformed data, keeping "coin_id" as the index.

#### 6. Finding the Optimal k using PCA Data
Repeat the Elbow Method using the PCA-transformed dataset.

Answer: How does the best k-value differ between the PCA and original datasets?

#### 7. Clustering Cryptocurrencies using PCA Data
Train K-Means on the PCA dataset using the best k.

Predict clusters and create a new DataFrame with the cluster labels.

Visualize clusters using hvPlot:

X-axis: "PC1"

Y-axis: "PC2"

Color: Cluster labels

Hover: "coin_id"

#### 8. Final Analysis
Compare results:

How does clustering change when using the PCA dataset vs. the original dataset?

Answer: What is the impact of using fewer features for K-Means clustering?

Technologies Used
Python

Pandas

Scikit-learn (StandardScaler, K-Means, PCA)

hvPlot

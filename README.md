# CryptoClustering

## Overview

This project uses unsupervised machine learning techniques to cluster cryptocurrencies based on their price change data over different time periods (24h, 7d, 30d, etc.). The primary objective is to identify groups of cryptocurrencies with similar price change behaviors. We apply **K-Means clustering** and **Principal Component Analysis (PCA)** to reduce the dimensionality of the data and find optimal clusters.

## Table of Contents

* [Installation](#installation)
* [Project Structure](#project-structure)
* [Data](#data)
* [Methodology](#methodology)
* [Steps and Code](#steps-and-code)
  * [1. Data Preprocessing](#1-data-preprocessing)
  * [2. Scaling the Data](#2-scaling-the-data)
  * [3. PCA for Dimensionality Reduction](#3-pca-for-dimensionality-reduction)
  * [4. K-Means Clustering](#4-k-means-clustering)
  * [5. Evaluation and Elbow Curve](#5-evaluation-and-elbow-curve)
  * [6. Visualization](#6-visualization)
* [Results](#results)
* [Conclusion](#conclusion)
* [License](#license)

## Installation

To run this project, you need to install the necessary Python libraries. The following libraries are used in the project:

`pip install pandas numpy matplotlib seaborn scikit-learn hvplot`

## Data

The dataset includes the following price change percentages for cryptocurrencies:

* `price_change_percentage_24h`
* `price_change_percentage_7d`
* `price_change_percentage_14d`
* `price_change_percentage_30d`
* `price_change_percentage_60d`
* `price_change_percentage_200d`
* `price_change_percentage_1y`

The `coin_id` column identifies each cryptocurrency.

## Structure

The project consists of the following key files and directories:

* `Crypto_Clustering.ipynb`: The main Python script where data preprocessing, clustering, and visualization tasks are handled.
* `Resources/`: Directory containing cryptocurrency data files (CSV).
* `requirements.txt`: A list of Python libraries required to run the project.

## Methodology

1. **Data Preprocessing** : The dataset is loaded and preprocessed, removing irrelevant columns and handling missing data.
2. **Scaling** : The data is scaled using **StandardScaler** to standardize the features before clustering.
3. **PCA** : **Principal Component Analysis (PCA)** is applied to reduce the dimensionality of the dataset.
4. **K-Means Clustering** : **K-Means** is used to group cryptocurrencies based on their price change patterns. The optimal number of clusters is determined using the  **Elbow Method** .
5. **Visualization** :

* **Elbow Curve** : The **Elbow Curve** is plotted to determine the best `k` (number of clusters).
* **Scatter Plot** : A 2D scatter plot is created using the first two principal components (PC1, PC2), colored by the cluster labels.

## Results

* The **Elbow Method** indicates the optimal number of clusters is `k=3`.
* The scatter plot visualizes how cryptocurrencies are grouped in 2D space based on their price change patterns, with each group represented by different colors.

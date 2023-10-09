# Module 19 Challenge: CryptoClustering

## CryptoClustering: Unsupervised Learning for Cryptocurrency Analysis:
This project uses unsupervised learning to compare clustering techniques using cryptocurrency data.

**Project Objective:**
To group cryptocurrencies based on their price change data using K-Means clustering and then visualize the results.

**Steps and Methodologies:**

**1. Data Loading and Exploration:**
Loaded the crypto_market_data.csv into a DataFrame.
Explored the data using summary statistics and plots to understand its distribution.

**2. Data Preparation:**
Normalized the dataset using the StandardScaler from scikit-learn.
Created a DataFrame with the scaled data, retaining the "coin_id" index from the original DataFrame.

**3. Determine Optimal k for Clustering:**
Used the elbow method to find the best k-value for K-Means clustering on the scaled data.
Initialized, fitted, and used the K-Means model to predict clusters based on the original scaled data.

**4. Visualize Clusters using hvPlot:**
A scatter plot was created using hvPlot to visualize clusters based on price change percentages.

**5. Optimizing Clusters using PCA:**
Conducted a Principal Component Analysis (PCA) to reduce the features of the original scaled data to three main components.
Created a DataFrame to hold the PCA data.

**6. Re-determining Optimal k after PCA:**
Repeated the elbow method to identify the optimal k-value using the PCA data.
Analyzed if the optimal k-value changed post PCA.

**7. Cluster Cryptocurrencies Post PCA:**
Initialized, fitted, and predicted clusters using the K-Means model on the PCA data.
Created another scatter plot using hvPlot to visualize the clusters after PCA.


## Key Questions Answered:##
What is the best value for k for the original and PCA data? **4**

What is the total explained variance of the three principal components in PCA? **89%**

What is the impact of using fewer features to cluster data with K-Means? 

While there appears to be overlap between certain clusters in both sets of analysis (Original clusters 0, 2, 3)(PCA clusters 0 and 1), the PCA method using fewer features appears to show clearer / more distint clusters. These distinct clusters potentially reveal inherent structures in the data by reducing noise and focusing on the most significant patterns. 


**Conclusion:**

This project successfully clustered cryptocurrencies based on their price change data. Through a combination of feature scaling, optimal cluster determination, and PCA, we were able to effectively group and visualize cryptocurrencies. The analysis provides insights into the behavior of cryptocurrencies and how they are affected by price changes over different periods.

**Tools and Libraries Used:**
- Python
- pandas
- scikit-learn
  - StandardScaler
  - KMeans
  - PCA
- hvPlot


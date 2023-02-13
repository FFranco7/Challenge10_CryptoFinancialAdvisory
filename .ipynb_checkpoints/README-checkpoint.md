# Challenge10_CryptoFinancialAdvisory

# Import necessary libraries
import pandas as pd
import hvplot.pandas
from pathlib import Path
from sklearn.cluster import KMeans
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler

# Import and load data to be analyzed
Use the read function and make a quick statistics analysis with describe()

# Plot data to see price change on different cryptocurrency pairs on the different timeframes
Make it with an interactive hv.plot

# Organize data
Normalize data --> Use StandardScaler() to normalize data and create a scaled data dataframe

# Find the best k value by:
1. Creating a list with k-values range
2. Creating an empty inertia list
3. Create a loop that will help determine the clustersin the elbow graph and store the elbow data in a dictionary
4. Plot the elbow curve and determine de optimal k value

# Cluster data of cryprtocurrencies by using kmeans original data
1. Initialize the K-Means model with four clusters using the best value for k
2. Fit the K-Means model using the original data
3. Predict the clusters to group the cryptocurrencies using the original data. View the resulting array of cluster values
4. Create a copy of the original data and add a new column with the predicted clusters
5. Create a scatter plot to identifty data clusters by color

# Optimize Clusters with Principal Component Analysis
1. Create a PCA model instance by setting n_components=3
2. Use the PCA model to reduce to three principal components. Use head() to view the first five rows of the DataFrame
3. Retrieve the explained variance to determine how much information can be attributed to each principal component
4. Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame

# Find the Best Value for k Using the PCA Data
Code the elbow method algorithm and use the PCA data to find the best value for k while using a range from 1 to 11.
Identify optimal value for k by plotting a line chart with all the inertia values computed with the different values of k.

# Cluster Cryptocurrencies with K-means Using the PCA Data
1. Use best k value to initialize model
2. Fit model with pca data
3. Group cryptocurrencies by predicting clusters.
4. Create new column in the df that includes the pca data and store predicted clusters
5. Create scatter plott

# Visualize and Compare the Results
Create and analyze the cluster analysis results by contrasting the outcome with and without using the optimization techniques. Create composite plots to contrast elbow curves and crypto clusters considering original and pca data.

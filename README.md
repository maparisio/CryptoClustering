# CryptoClustering

## Module 19 Challenge - Unsupervised-Learning

##### In this challenge, I will use my knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. These are the guidelines I am using to get my answers:

## Index
1. Content of the repository
2. Instructions for the Project
3. References

### Content of the repository
  * Resources Directory:
    - crypto_market_data.csv
  * Images Directory:
    - composite_elbow_plot.png
    - composite_scatter_plot.png
    - elbow_plot.png
    - line_plot.png
    - pca_elbow_plot.png
    - pca_scatter_plot.png
    - scatter_plot.png
  * Coding and plotting file:
    - Crypto_Clustering.ipynb
### Instructions
  1. Rename the 'Crypto_Clustering_starter_code.ipynb' file as 'Crypto_Clustering.ipynb'.
  2. Load the crypto_market_data.csv file into a DataFrame.
  3. Get the summary statistics and plot the data to see what the data looks like before proceeding.
     
### FIND THE BEST VALUE FOR k USING THE ORIGINAL SCALED DATAFRAME
* Use the elbow method to find the bets value for 'k' using the following steps:
  - Create a list with the number of k values from 1 to 11.
  - Create an empty list to store the inertia values.
  - Create a 'for' loop to compute the inertia with each possible value of 'k'.
  - Create a dictionary with the data to plot the elbow curve.
  - Plot a line chart with all the inertia values compute with the different values of 'k' to visually identify the optimal value for 'k'.
  - Answer the following question in your notebook: What is the best value for 'k'?

### CLUSTERING CRYPTOCURRENCIES WITH K-MEANS USING THE ORIGINAL SCALED DATA
* Use the following steps to cluster the cryptocurrencies for the best value for 'k' on the original scaled data:
  - Initialize the K-means model with the best value for 'k' • Fit the K-means model using the original scaled DataFrame.
  - Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
  - Create a copy of the original data and add a new column with the predicted clusters.
* Create a scatter plot using hvPlot as follows:
  - Set the x-axis as "PC1" and the y-axis as "PC2".
  - Color the graph points with the labels found using K-means.
  - Add the "coin_id" column in the "hover_cols" parameter to identify the cryptocurrency represented by each data point.

### OPTIMIZE CLUSTERS WITH PRINCIPAL COMPONENT ANALYSIS
* Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
* Retrieve the explained variance to determine how much information can be attributed to each principal component, and then answer the following question in your notebook:
  - What is the total explained variance of the three principal components?
* Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## FIND THE BEST VALUE FOR k USING THE PCA DATA
* Use the elbow method on the PCA data to find the best value for 'k' using the following steps: 
  - Create a list with the number of k-values from 1 to 11.
  - Create an empty list to store the intertia values.
  - Create a 'for' loop to compute the inertia with each possible value of 'k'.
  - Create a dictionary with the data to plot the Elbow curve.
  - Plot a line chart with all the inertia values computed with the different values of 'k' to visually identify the optimal value for 'k'.
* Answer the following questions in your notebook:
  - What is the best value for 'k' when using the PCA data?
  - Does it differ from the best k value found using the original data?

CLUSTER CRYPTOCURRENCIES WITH K-MEANS USING THE PCA DATA
* Using the following steps to cluster the cryptocurrencies for the best value for 'k' on the PCA data:
  - Initialize the K-mans model with the best value for 'k'.
  - Fit the K-means model using the PCA data.
  - Predict the clusters to group the cryptocurrencies using the PCA data.
  - Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
* Create a scatter plot using hvPlot as follows:
  - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
  - Color the graph points with the labels found using K-means.
  - Add the "coin_id" column in the "hover_cols" parameter to identify the cryptocurrency represented by each data point.
* Answer the following question:
  - What is the impact of using fewer features to cluster the data using K-Means?




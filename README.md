# CryptoClustering

## Before You Begin

1. Create a new repository for this project called CryptoClustering. Do not add this homework to an existing repository.

2. Clone the new repository to your computer.

3. Push your changes to GitHub.


## Instructions

1. Rename the Crypto_Clustering_starter_code.ipynb file as Crypto_Clustering.ipynb.

2. Load the crypto_market_data.csv into a DataFrame.

3. Get the summary statistics and plot the data to see what the data looks like before proceeding.

## Prepare the Data

-Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

-Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

   -The first five rows of the scaled DataFrame should appear as follows:
   ![image](https://github.com/user-attachments/assets/2b8b8d93-8aba-4919-b5fd-e8f3733e679a)
   

#### Find the Best Value for k Using the Scaled DataFrame

Use the elbow method to find the best value for k using the following steps:

1. Create a list with the number of k values from 1 to 11.
   
2. Create an empty list to store the inertia values.
   
3. Create a for loop to compute the inertia with each possible value of k.
   
4. Create a dictionary with the data to plot the elbow curve.

5. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
   
6. Answer the following question in your notebook: What is the best value for k?
   
#### Cluster Cryptocurrencies with K-means Using the Scaled DataFrame
Use the following steps to cluster the cryptocurrencies for the best value for k on the scaled DataFrame:

1. Initialize the K-means model with the best value for k.
   
2. Fit the K-means model using the scaled DataFrame.
   
3. Predict the clusters to group the cryptocurrencies using the scaled DataFrame.
   
4. Create a copy of the scaled DataFrame and add a new column with the predicted clusters.
   
5. Create a scatter plot using hvPlot as follows:
   
---Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
---Color the graph points with the labels found using K-means.
---Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

### Optimize Clusters with Principal Component Analysis

1. Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.

2. Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:

-- What is the total explained variance of the three principal components?

3. Create a new DataFrame with the scaled PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

--The first five rows of the scaled PCA DataFrame should appear as follows:

![image](https://github.com/user-attachments/assets/cdd40177-5624-44e3-abd3-6c6f2b4d7032)


### Find the Best Value for k Using the PCA DataFrame

Use the elbow method on the scaled PCA DataFrame to find the best value for k using the following steps:

1. Create a list with the number of k-values from 1 to 11.
   
2. Create an empty list to store the inertia values.

3. Create a for loop to compute the inertia with each possible value of k.

4. Create a dictionary with the data to plot the Elbow curve.

5. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

6. Answer the following question in your notebook:

---What is the best value for k when using the scaled PCA DataFrame?

---Does it differ from the best k value found using the original scaled DataFrame?

### Cluster Cryptocurrencies with K-means Using the PCA DataFrame

Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA DataFrame:

1. Initialize the K-means model with the best value for k.

2. Fit the K-means model using the scaled PCA DataFrame.

3. Predict the clusters to group the cryptocurrencies using the scaled PCA DataFrame.

4. Create a copy of the scaled PCA DataFrame and add a new column to store the predicted clusters.

5. Create a scatter plot using hvPlot as follows:

---Set the x-axis as "PC1" and the y-axis as "PC2".

---Color the graph points with the labels found using K-means.

---Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

6. Answer the following question:
---What is the impact of using fewer features to cluster the data using K-Means?


### Resources

Class

ChatGPT

Missha Vara

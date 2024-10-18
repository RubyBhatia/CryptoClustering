# CryptoClustering
Challenge-19

**Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.**

Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame. The first five rows of the scaled DataFrame should appear as follows:
<img width="671" alt="image" src="https://github.com/user-attachments/assets/0448d13c-df18-4cfc-865d-3772cbcb15ea">

**Find the Best Value for k Using the Scaled DataFrame**
Use the elbow method to find the best value for k using the following steps:

1. Create a list with the number of k values from 1 to 11.
2. Create an empty list to store the inertia values.
3. Create a for loop to compute the inertia with each possible value of k.
4. Create a dictionary with the data to plot the elbow curve.
5. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal 
   value for k.

<img width="657" alt="image" src="https://github.com/user-attachments/assets/b9e739be-3b6c-48e1-bd35-fa7d42101408">

Question: What is the best value for k?

Answer: The optimal value for k is 4 because the graph starts to plateau after this point, meaning any increase in accuracy with higher k values is outweighed by a decrease in the efficiency of the analysis.

<img width="569" alt="image" src="https://github.com/user-attachments/assets/3a22579d-8b29-4de1-b969-68e257848bae">

**Cluster Cryptocurrencies with K-means Using the Scaled DataFrame**
Use the following steps to cluster the cryptocurrencies for the best value for k on the scaled DataFrame:

1. Initialize the K-means model with the best value for k.
2. Fit the K-means model using the scaled DataFrame.
3. Predict the clusters to group the cryptocurrencies using the scaled DataFrame.
4. Create a copy of the scaled DataFrame and add a new column with the predicted clusters.
5. Create a scatter plot using hvPlot as follows:
  - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
  - Color the graph points with the labels found using K-means.
  - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

**Cluster Cryptocurrencies with K-means Using the PCA DataFrame**
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA DataFrame:

Initialize the K-means model with the best value for k.
Fit the K-means model using the scaled PCA DataFrame.
Predict the clusters to group the cryptocurrencies using the scaled PCA DataFrame.
Create a copy of the scaled PCA DataFrame and add a new column to store the predicted clusters.
Create a scatter plot using hvPlot as follows:
Set the x-axis as "PC1" and the y-axis as "PC2".
Color the graph points with the labels found using K-means.
Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.










# Challenege_10


**Background**

In this Challenge, I assumed the role of an advisor in one of the top five financial advisory firms in the world. Competitors are fierce, so I want to propose a novel approach to assembling investment portfolios that are based on cryptocurrencies. Instead of basing my proposal on only returns and volatility, I wanted to include other factors that might impact the crypto market—leading to better performance for possibel portfolios.


**What I Created**

In this Challenge, I combined my financial Python programming skills with the new unsupervised learning skills that I acquired in this module.

I created a Jupyter notebook that clusters cryptocurrencies by their performance in different time periods. I then plotted the results so that I could visually show the performance to the board.



**Instructions**

I used the starter code file to complete the tasks outlined in the Instructions. The steps for this Challenge are divided into the following sections:

1. Import the Data (provided in the starter code)
2. Prepare the Data (provided in the starter code)
3. Cluster Cryptocurrencies with K-means
4. Find the Best Value for k
5. Optimize Clusters with Principal Component Analysis
6. Visualize the Results


**Cluster Cryptocurrencies with K-means**

In this section, I used the K-Means algorithm with a given value for k to cluster the cryptocurrencies according to the price changes of cryptocurrencies provided.
Initializing the K-means model with four clusters (n_clusters=4).
I then fitted the K-means model using the scaled data.
predicting the clusters to group the cryptocurrencies using the scaled data. 
I then added a new column to the DataFrame with the predicted clusters.
I created a scatter plot using hvPlot by setting x="price_change_percentage_14d" and y="price_change_percentage_1y". I then colored the graph points with the labels found using K-Means and add the crypto name in the hover_cols parameter to identify the cryptocurrency represented by each data point.

**Find the Best Value for k**

In this section, I will use the elbow method to find the best value for k.
I coded the elbow method algorithm to find the best value for k then used a range from 1 to 11.
I then ploted a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.



**Optimize Clusters with Principal Component Analysis**

In this section, I will perform a principal component analysis (PCA) and reduce the features to three principal components.
I Created a PCA model instance and set n_components=3.
I used the PCA model to reduce to three principal components and viewed the first five rows of the DataFrame.
I retrieved the explained variance to determine how much information can be attributed to each principal component.
Finally creating a new DataFrame with the PCA data. 
I then initiated a new K-means algorithm using the PCA DataFrame to group the cryptocurrencies. I set the n_components parameter equal to the best value for k found before. 
For further analysis, I added the following columns to the DataFrame with the PCA data. Then reviewed the resulting DataFrame once the additional columns have been added. I did the following:
1.Added the price_change_percentage_1y and price_change_percentage_14d columns.
2.Added a column with the predicted cluster values identified using a k value of 4. 
3.Added a column with the predicted cluster values identified using the optimal value for k.

**Visualize the Results**

I performed the following:
1. In the first plot, I colored the plot points by the cluster values identified using a k value of 4.
2. In the second plot, I colored the plot points by the cluster values identified using the optimal value for k.
3. In both plots, I added the crypto name by sing the hover_cols parameter to identify the cryptocurrency represented by each data point.



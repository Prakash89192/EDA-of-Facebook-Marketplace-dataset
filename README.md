# EDA-of-Facebook-Marketplace-dataset
## Dataset information:
+ 16 data columns with 7050 entries.
+ The column names include the following: “status_id, status_type, status_published, num_reactions, num_comments, num_shares, num_likes, num_loves, num_wows, num_hahas, num_sads, num_angrys, Column1, Column2, Column3, Column4”.

## Data Cleaning
+ Since the columns ‘Column1, Column2, Column3, Column4’ doesn’t have any data drop these columns.
+ Change the datatype of ‘status_published’ to datetime for easy analysis.
+ Making sure that no NaN values are present in the dataset.
+ Now, after cleaning the data, the data will have 12 rows and 7050 entries.

## Feature scaling
+ Before we go with K-Means algorithm the data needs to be scaled.
+ For scaling the standardisation method is used.
+ StandardScaler is imported from sklearn.preprocessing.

## K-Means Clustering
+ The sklearn.cluster library is where the class KMeans is loaded from. The model was given a range of cluster numbers, from 1 to 10, in order to determine the ideal number of clusters for the dataset.
+ To prevent the Random Initialization Trap, the 'k-means++' method should be provided to the init parameter. The default settings for the max_iter and n_init were passed.
+ To determine the ideal number of clusters, the Within Cluster Sum of Squares, or WCSS, was calculated and shown. To determine the ideal number of clusters, the "Elbow Method" was applied.
+ When the ideal number of clusters was determined, the model was reinitialized and the ideal number of clusters was provided in using the n_cluster parameters.


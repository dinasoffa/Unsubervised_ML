# Unsubervised_ML

### Clustering Paradigms:

1-Representative-based
2-Hierarchical
3-Density-based
4-Graph-based
5-Spectral clustering


## 1- Clustering Paradigms : Representative-based "K-mean":
One of the simplest and most popular unsupervised machine learning algorithms
K-means is a greedy algorithm that minimizes the squared distance of points from their respective cluster means
It performs hard clustering, that is, each point is assigned to only one cluster. 
K-means can be used for nonlinear clusters. 

### implementation:
1-K is chosen as the number of clusters we wish to cluster our data into
2-Randomly choose centroid for each cluster
3-Iterate over the following two steps:
4-Cluster Assignment:
	- Assign data to the cluster whose centroid is closest
5-Centroid Adjustment:
	- Move each centroid to the mean of data assigned to its cluster


## 2-Hierarchical Clustering
Is an approach to build hierarchy of clusters based on hierarchical relationships between datapoints
Is a deterministic process: cluster assignments won’t change by running algorithm multiple times on the same input data

Can be implemented by either a bottom-up or top-down approach:
a-Agglomerative Clustering
b-Divisive Clustering

### a-Agglomerative Clustering implementation:
Idea: ensures near-by points end up in the same cluster
Algorithm
Initially, each data instance represents a Cluster
Repeat:
1-Pick the two closest clusters
2-Merge them into a new cluster
3-Stop when there is only one cluster left
4-Produces a family of clusters represented by a Dendrogram


## 3-Density-based Clustering DBSCAN:
Works on the assumption that clusters are dense regions in space separated by regions of high density
Identifies clusters according to local density of data points
Identifies noise points as separate cluster
Doesn’t need to pre-assign the number of clusters

Requires only 2 parameters:
1-Epsilon
Is the radius of the circle to be created around each data point to check the density
2-MinPoints
Is the minimum number of data points required inside that circle for that data point to be classified as a Core point

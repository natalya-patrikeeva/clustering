Clustering technique for airlines market segmentation

In this project, I use hierarchical and K-means clustering to find similar groups
 of customers that belong to a frequent flyer program. Then we can design a
 marketing strategy (for example, different mileage offers) targeted specifically
 at each group.

The data AirlinesCluster.csv is from the textbook "Data Mining for Business Intelligence,"
by Galit Shmueli, Nitin R. Patel, and Peter C. Bruce. The file contains
information on 3,999 members of the frequent flyer program and 7 variables.

The variables are described below:

Balance = number of miles eligible for award travel

QualMiles = number of miles qualifying for TopFlight status

BonusMiles = number of miles earned from non-flight bonus transactions in the past 12 months

BonusTrans = number of non-flight bonus transactions in the past 12 months

FlightMiles = number of flight miles in the past 12 months

FlightTrans = number of flight transactions in the past 12 months

DaysSinceEnroll = number of days since enrolled in the frequent flyer program


First, I normalize the data using the caret package and preProcess function
before running the clustering algorithms so that the data is not dominated by
the variables with large values. After normalization, all variables have mean 0
 and standard deviation of 1.

Clustering

For comparison, I run hierarchical clustering and K-means clustering with 5
clusters. Plotting the dendrogram helps us to determine how many clusters to
choose. Comparing the centroids of the clusters, we conclude that:
 - Cluster 1 has the largest average DaysSinceEnroll value and
describes infrequent but loyal customers.
 - Cluster 2 has the largest average QualMiles, FlightMiles, and FlightTrans
 values and describes customers who have accumulated a large amount of miles,
 and the ones with the largest number of flight transactions.
 - Cluster 3 has the largest average Balance, BonusMiles, BonusTrans values and
 describes customers who have accumulated a large amount of miles, mostly through
 non-flight transactions.
 - Cluster 4 has no largest values and describes relatively new customers who
seem to be accumulating miles, mostly through non-flight transactions.
 - Cluster 5 has no largest values and describes relatively new customers who
 don't use the airline very often.

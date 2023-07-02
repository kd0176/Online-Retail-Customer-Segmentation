# Online-Retail-Customer-Segmentation
This is a AlmaBetter's capstone project and the topic is Online Retail Customer Segmentation, which is a unsupervised machine learning task.
In this project, our task is to identify major customer segments on a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

## The need of customer segmentation:
Customer segmentation is essential for businesses to optimize marketing efforts, enhance customer experiences, allocate resources efficiently, drive innovation, gain a competitive edge, and improve customer retention and acquisition. It helps businesses understand their customers better and tailor their strategies to meet their specific needs, ultimately leading to improved business performance.

## Recency-Frequency-Monetary (RFM) model to determine customer value:
The RFM model is a customer segmentation approach that uses three metrics: recency, frequency, and monetary value. (**Recency – How recently did the customer purchase? Frequency – How often do they purchase? Monetary Value – How much do they spend?**) It helps businesses determine the value of customers based on their recent activity, purchase frequency, and spending. By assigning scores to each metric and combining them, customers can be categorized into segments. This segmentation allows businesses to prioritize marketing efforts, retain high-value customers, target potential high-value customers, re-engage at-risk customers, and decide how to handle low-value customers.

## Segmentation with K-means clustering:
In the customer segmentation process using K-means clustering, the data undergoes exploratory analysis, preprocessing, feature engineering, and standardization. The K-means algorithm is then applied to determine customer segments. **Silhouette analysis**, **Elbow curve** and cluster visualizations help determine the optimal number of clusters (K) in the algorithm. The insights and observations from the results are thoroughly discussed to draw meaningful conclusions from a business perspective.
 
## Segmentation with Hierarchical clustering:
Segmentation with hierarchical clustering involves grouping customers into segments based on similarities in their attributes or behaviors. The algorithm creates a hierarchical structure of clusters by merging or splitting data points. After preprocessing the data and selecting relevant variables, hierarchical clustering is performed. A **dendrogram**, which is a visual representation of the clustering process, helps determine the number of clusters.

## Conclusion:
We started with RFM model and segmented customers into different groups based on their recency, frequency and monetary value. we devided customers in different groups by assigning RFM_group and by calculating RFM_score.

* RFM_group : RFM_group is combined concatenated score of R, F and M scores, where 444 represents best and 111 represents worst.
* RFM_score : RFM_score is total sum of R, F and M scores, where 12 is highest and best score and 3 is lowest and worse score.

After that we used Kmeans clustering algorithm, used silhouette and elbow method to determine the optimal number of clusters and formed 3 clusters.

* first cluster label_0 contains 3258 customers with average recency of 40, average frequency equals to 103, and average monetary is around 1950 dollars.
* second cluster label_1 contains 1100 customers with average recency of 247 and minimun recency of 138 which means these customers have not made any purchase in last 4 months, average frequency is 27 only, and average monetary is around 472 dollars which is also very low in comparison of cluster_0.
* third cluster label_2 contains only 12 customers with max recency of 25 and average recency 5 only which is very good, average frequency equals to 2813, and average monetary is more than 100k dollars which are very high compared to cluster_0 and cluster_1.
  
Then we used agglomerative hierarchical clustering algorithm, by dendogram found optimal number of clusters and formed 3 clusters again, these clusters were similar to clusters formed by kmeans. at the end we give name to these clusters Premium customers, regular customers and not so regular customers.

* Premium customers : Customers having very high monetary and frequency with low recency.
* Regular customers : Customers having decent monetary and frequency with moderate recency.
* Not so regular customers : Customers have not made any purchase in last 4-5 months, also with low frequency and low monetary value.

  

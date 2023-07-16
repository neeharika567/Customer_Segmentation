
# Customer Segmentation
Customer segmentation is the practice of dividing a company’s customers into groups that reflect similarity among customers in each group.

**Workflow of the project**
---

**Customer data** - I have used the *Mall Customer Segmentation Data* dataset from kaggle which is created specifically for learning customer segmentation concepts, also known as *Market Basket Analysis* . 
[Click here too see dataset. ](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)


**Data Pre-processing and Data Analysis** - I take the annual income and spending score column from the dataset and I try to find the initial number of clusters using the *Within Clusters Sum of Squares(WCSS)*. The *WCSS* is a measure of the variability of the observations within each cluster. In general, a cluster that has a small sum of squares is more compact than a cluster that has a large sum of squares.

![img](https://149695847.v2.pressablecdn.com/wp-content/uploads/2019/08/4_wcss.png)

I later plot a *WCSS vs Number of Clusters* graph to find the optimal number of clusters for my analysis. This graph is also called the **Elbow Point Graph** . That value of k(number of centroids) is chosen from where the graph starts to look like a straight line. The value of k in this project is 5.

![elbow point](https://github.com/neeharika567/Customer_Segmentation/assets/111648731/7acd3a17-1bf0-424e-833b-93a62fbc238c)


**Training** - Finally I train my model and each value will get a label based on their similarities and differences with each other.

*kmeans = KMeans(n_clusters=5, init='k-means++', random_state=0)*

*Y = kmeans.fit_predict(X)*

The above statements load the K-Means model in kmeans variable and fit each value of X in the five different clusters.

**Visualization** - The final visualization of the project is as follows:

![clustering](https://github.com/neeharika567/Customer_Segmentation/assets/111648731/588fa963-8ca4-49f1-8055-83627b71589a)

You can more about this concept form the link provided.
[Learn more about K-Means Clustering here.](https://www.javatpoint.com/k-means-clustering-algorithm-in-machine-learning)














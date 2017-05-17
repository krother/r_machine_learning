# k-Means Clustering

This is probably the most basic clustering method. In **k-means clustering**, you decide how many clusters you want. The algorithm then does the following:

1. set random starting centers for each cluster
2. assigns each data point to the closest cluster center
3. sets each cluster center to the mean of its assigned data points
4. iterate 2.+3. until the cluster assignment does not change any more.

### Caveats

k-means clustering is a solid method if you keep a few things in mind:

* The clusters are roughly spherical.
* The algorithm does not tell you whether the number of clusters you chose was good or not.
* The initial points are random, so the algorithm might converge on different cluster centers, depending on the random seed.
* The clustering is based on a distance measure. With many dimensions, this works very badly.

### Code

`library("ggplot2")`

`library("class")`

``

`# set the seed to make your analysis reproductible`

`set.seed(123)`

``

`data("iris")`

`m = as.matrix(iris)`

``

``

`# build a kmeans model`

`kmeans_model <- kmeans(x=m[,1:4], centers=3)`

``

`kmeans_model["centers"]`

`kmeans_model["cluster"]`

`iris <- transform(iris, cluster=kmeans_model["cluster"])`

``

`ggplot(iris, aes(x=Sepal.Width, y=Petal.Width, color = cluster), size = 3) + geom_point()`






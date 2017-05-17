# Principal Component Analysis \(PCA\)

**PCA** is a method for dimensionality reduction. It tries to transform a multidimensional dataset in such a way that one dimension represents as much of the variance in the data as possible. This allows you to represent data by a few representative dimensions, the **principal components**.

Each principal component is a vector mapping the original dimensions to the transformed dimensions. PCA can calculate multiple principal components to give you a more accurate description of the data.

### Example:

Imagine you have data on a number of **ships**. Each ship has a number of descriptors: length, width, height, BRT, depth, number of crew members, engine strength etc. PCA allows you to summarize all these numbers to one number. With ships, it will roughly correspond to the size of the ships, because most of the other numbers grow with bigger ship size.

### PCA is useful if you want to:

* visualize multidimensional data
* simplify a complex dataset
* get an impression what the shape of your data is
* speed up calculations 

PCA is usually quite useless if your data has only 2-3 dimensions.

### Code

`data(iris)`

`  
`

`iris.log <- log(iris[, 1:4])`

`iris.species <- iris[, 5]`

`  
`

`iris.pca <- prcomp(iris.log, center = TRUE, scale. = TRUE)`

`  
`

`print(iris.pca)`

`plot(iris.pca, type = "l")`

`  
`

`summary(iris.pca)`

### Also see:

[https://tgmstat.wordpress.com/2013/11/28/computing-and-visualizing-pca-in-r/](https://tgmstat.wordpress.com/2013/11/28/computing-and-visualizing-pca-in-r/)


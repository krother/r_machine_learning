# Support Vector Machines \(SVM\)

**Support Vector Machines** are a type of classification model that calculates a coordinate transformation of the data known as the **kernel trick**. On the transformed data, a **hyperplane** is used to divide the data for classification. In contrast to logistic regression, the shape of the classification boundary is not limited. To construct the boundary, a SVM selects a number of \_"important" \_points, the **support vectors **\(hence the name\).

SVMs can work with high-dimensonal datasets. They tend to be bit sensitive to parameters \(type of kernel, regularization hyperparameter\).

### Code

`library("e1071")`

`  
`

`data(iris)`

`  
`

`x <- subset(iris, select=-Species)`

`y <- iris[,"Species"]`

`  
`

`model <- svm(x, y)`

`print(model)`

`summary(model)`

`  
`

`# check accuracy`

`pred <- predict(model, x)`

`table(pred, y)`

`  
`

`# color by class`

`# mark support vectors by +`

`plot(cmdscale(dist(iris[,-5])),`

`col = as.integer(iris[,5]),`

`pch = c("o","+")[1:150 %in% model$index + 1])`


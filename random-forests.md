# Random Forests

Random Forests are a versatile method for classification and regression. It is an extension of **decision trees**. Decision trees are very prone to overfitting. To avoid this problem, Random Forests do the following:

* use many trees instead of one
* use a bootstrapped random subset of the data points in each tree \(same size, duplicates may occur\).
* use a random sub-sample of the available features in each tree.

For prediction, the trees cast a majority vote on the result.

    library(randomForest)

    rf_model <- randomForest(as.factor(TargetColumn) ~ Col1 + Col2 + Col3,

                    data=training, importance=TRUE, ntree=10)

    # evaluate model
    rf_model.results <- predict(rf_model,newdata=Xtest,type='response')
    misClasificError <- mean(rf_model.results != ytest)
    print(paste('Accuracy Training',1-misClasificError))

    Prediction <- predict(rf_model, test)

### Hints

* The main parameter is the number of trees
* Also see [http://trevorstephens.com/kaggle-titanic-tutorial/r-part-5-random-forests/](http://trevorstephens.com/kaggle-titanic-tutorial/r-part-5-random-forests/)
*  randomForest can do regression as well, set type='regression'!

To plot some properties of the trees, try

`varImpPlot(rf_model)
`

The **gini diagram** quantifies the purity of end nodes
 in the tree \(i.e. whether there is consensus on the result\)

### Caveats

Note that if you use a Random Forest for regression, it will be unable to extrapolate beyond the value range it was shown.




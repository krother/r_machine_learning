# k-Nearest-Neighbors

**k-nearest-neighbors** or **knn** is arguably one of the most simple predictive models for **classification**. Given a training set and a new data point, it looks for the _closest k data points_ and predicts whatever class the majority of them has. Typical values for _k_ are 1, 3 and 5.

### Code

`library("class")`

`# set a seed value to make your analysis reproductible`

`set.seed(123)`

`data("iris")`

`m = as.matrix(iris)`

`# training/test split`

`size <- floor(nrow(m) * 0.75)`

`index <- sample(seq_len(nrow(m)), size = size)`



`train <- m[index, ]`

`test <- m[-index, ]`

`Xtrain = train[,1:4]`

`ytrain = train[,5]`

`Xtest = test[,1:4]`

`ytest = test[,5]`



`# build k-nearest-neighbor model`

`predicted <- knn(train=Xtrain, test=Xtest, cl=as.factor(ytrain), k=3)`

`# evaluate prediction`

`correct = ytest == predicted`

`sum(correct) / length(correct)`

**knn** is useful as a baseline to compare other models.


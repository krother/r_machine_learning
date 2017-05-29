# Calculating RMSE

Given an array of predicted and reference values, you may want to calculate the **root mean square error **\(also called RMSD\).: 

`validation = c(2.2, 3.3, 4.4, 5.5)`

`predicted = c(2.1, 3.5, 4.2, 5.6)`

``

`error <- validation - predicted`

`rmse <- sqrt(mean(error^2))`

`print(rmse)`




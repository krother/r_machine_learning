# Dummy Encoding

For some ML methods it is helpful to transform a column with categories into multiple categories with binary values. 

For instance, we have a column `crop` that contains the values `barley, wheat` and `rice`.

With **dummy encoding**, we create three columns `crop_barley,`_` crop_wheat` and `crop_rice`_, each having values 0 or 1.

`crops <- c("wheat", "rice", "rice", "wheat", "barley", "rice", "rice")`

`sizes <- c(3, 5, 6, 3, 4, 2, 2)`

``

`# format as data frame`

`data <- data.frame(crop=crops, size=sizes) `

`table(data)`

``

`# dummy encoding`

`dummies <- model.matrix(~crops-1, data=data)`

`dummies`

``

`data$crops = dummies`




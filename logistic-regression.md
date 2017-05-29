# Logistic Regression

Despite its name, Logistic Regression is a method for **classification**. It is conceptually similar to linear regression. However, because we want to model discrete categories, the **logistic function **\(a sigmoid curve\) represents alternating between categories better.

While building the model, a threshold value where the sidmoid curve sharply raises is optimized.

In R, the **generalized linear model** function `glm()` creates logistic regressions:

`model <- glm(Y ~.,family=binomial(link='logit'), data=training)`

`summary(model)`

``

`result <- predict(model,newdata=Xtest,type='response')`

`result <- ifelse(result > 0.5,1,0)`

### Hints

* One key advantage of the method is that you obtain **coefficients** for each input feature that are easy to interpret. 
* Each coefficient is accompanied by a **probability** that describes statistical significance 
* Logistic Regression can handle multiple categories
* also see [https://www.r-bloggers.com/how-to-perform-a-logistic-regression-in-r/  ](https://www.r-bloggers.com/how-to-perform-a-logistic-regression-in-r/)




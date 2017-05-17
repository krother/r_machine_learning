# Basic Concepts

## Overfitting

**Overfitting **means that a model adapts to training data too well. By _memorizing most of the training data_, the model is unable to generalize. As a result, the model will perform well on training data, but perform badly on independent test data. Overfitting is a serious risk to the practical usage of machine learning models.

#### Solutions:

* Add more data
* Reduce the complexity/number of parameters of the model
* Increase regularization or tweak other hyperparameters
* Choose a less complex type of model

# Underfitting

**Underfitting** refers to a situation where the model is _too simple_. It does not fully utilize the information in the data. As a result, the model does not perform well on the training set.

#### Solutions:

* Allow the model to have more parameters
* Reduce regularization or tweak other hyperparameters
* Choose a more complex type of model

## Parameter Search

It is possible to try a series of values for a model parameter to find out which of them gives the best result. This is called **parameters search **or **grid search**. When doing parameter search, you **must** keep an independent portion of the data as a **validation set** that is not used at all during the parameter search. Otherwise you will over-optimize the model.

The validation set is used only at the very end to measure the quality of the resulting model.




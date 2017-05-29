# Scaling

Many machine learning methods \(SVM, neural networks, clustering algorithms, PCA\) require data to be **scaled**. The values need to be brought into the same range, e.g. to make columns of a different order of magnitude comparable.

Two types of scaling are widely used:

### Scaling to mean=0 and variance=1

The default of the `scale` function:

`x <- c(1,2,3,4,5,6,7)`

`xscaled <- scale(x)`

### Scaling to mininum=0 and maximum=1

```
xscaled = scale(x, center=min(x), scale=max(x)-min(x))
```




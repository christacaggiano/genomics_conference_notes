# Keynote II
## Matthew Stephens
## Reflections on some projects in computational biology

* research is non-linear and non-monotonic, but we present it as linear and monotonic
* PCA - genes mirror geography
* started with question - what happens when you do pca on spatial data
* circulant matrices - one in which each column is a cyclic shift of the previous one
* All nxn circulant matrices have the same eigenvector - and they are columns of he nxn fourier transform matrix
* for a linear habitant, distance matrix is circulant
* Shrinkage estimation - http://varianceexplained.org/r/empirical_bayes_baseball/
* extremes of a dataset are often ones with the largest measurement error
* shrinkage - shrinking towards some mean (in genetics often shrink effect sizes to 0)
* "black box" shrinkage via empirical bayes

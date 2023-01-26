### My answers to cracking the machine learning interview

#### Learning Theory

- Describe Bias and variance with example : `We can define the bias of an estimator as the difference between the expectation of a function of the data and the true parameter defining the data generating distribution.` Example the `bias` of a `Bernoulli` distribution. The `variance` of an estimator defines how the estimator computed from the sample data varies, once we resample the dataset from the underlying data generating distribution.
-  What is emperical risk minimization: `The empirical risk minimization is a minimization problem which involve selecting a class of function that minimizes the average error over the training set`
-  Formular for training error and Generalization error and differences: The `training` error is the expected value of the error over the training input, whereas the `generalization error` is over the test input.
-  Uniform convergence in machine learning : A class of functions $\left(f_{n}\right)$
is said to be uniformly convergence to $f$ for a data set $E$ if for all $\epsilon >0$, there exist $n$ such that for $n>N$, $\left|\left|f_{n}-f\right|\right|< \epsilon$.
- Error bound of the `uniform convergence` : $\left|\left|f_{n}-f\right|\right| \leq \frac{f^{n+1}(x)}{(n+1)!}$

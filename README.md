### My answers to cracking the machine learning interview

#### Learning Theory

- Describe Bias and variance with example : `We can define the bias of an estimator as the difference between the expectation of a function of the data and the true parameter defining the data generating distribution.` Example the `bias` of a `Bernoulli` distribution. The `variance` of an estimator defines how the estimator computed from the sample data varies, once we resample the dataset from the underlying data generating distribution.
-  What is emperical risk minimization: `The empirical risk minimization is a minimization problem which involve selecting a class of function that minimizes the average error over the training set`
-  Formular for training error and Generalization error and differences: The `training` error is the expected value of the error over the training input, whereas the `generalization error` is over the test input.
-  Uniform convergence in machine learning : A class of functions $\left(f_{n}\right)$
is said to be uniformly convergence to $f$ for a data set $E$ if for all $\epsilon >0$, there exist $n$ such that for $n>N$, $\left|\left|f_{n}-f\right|\right|< \epsilon$.
- Error bound of the `uniform convergence` : $\left|\left|f_{n}-f\right|\right| \leq \frac{f^{n+1}(x)\left(x-c\right)^{n}}{(n+1)!}$
- The `Bias-variance trade-off`: The trade-off between minimizing both the bias and the variance of given model, knowing that a high variance will lead to `overfitting` and high `bias` will lead to `underfitting`. The variance and bias are closely related to the train error knowing that $MSE= bias^{2}+ variance+ \epsilon$, where $\epsilon$ is the irrudicible noise.
- What is the `VC` dimension:  It's an informal term for the measurement of a `model's capacity`
- What does the training set size depend on for a finite and infinite hypothesis set? Compare and contrast.? The training set size depends on a finite number of data points for a finite hypothesis set (base on the vc dimension hypothesis, from my intuition).
- What is the VC dimension of an n-dimensional linear classifier? The VC dimension of an n-dimensional linear classifier is at least `n+1` 

#### Model Selection

- Why are model selection methods needed?: We want to identify and select  the best model from the hypothesis space that maximizes the performance of the learning algorithm (or minimizes the generalization error). This can usually be performed using feature selection techniques.
- How do you trade-off bias and variance?: we can use a shrinking method that reduces the value of the weight of our learning algorithm, which will lead to a decrease in variance with a substantial increase in the bias. (like a kind of regularization technique).
- What is cross-validation?: CV is machine learning technique that involve training a model on a sub portion of the train-data and evaluate in another subset with the objective of mitigating overfitting and improve generalization.
- Describing different cross-validation techniques:
1. K-fold cross validation:



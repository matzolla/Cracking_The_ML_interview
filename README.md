### Some ML notes

### Learning Theory

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
- Describing different cross-validation techniques: $\bullet$ `K-fold cross validation`: In `k-fold` cross validation, the data set is randomly split into k-fold where by one fold is used for evalution and the remaining `k-1` folds are used for training the model,the error $E_{k}$ is stored and the process is repeated for the remaining folds. At the end we average the error over the `k`-folds. We also have `LOOCV` similar to k-fold just that the fold here is `1point` the training is done on the other `n-1` points.
- Why is feature selection required?: reduces overfitting, improve accuracy performance also reduces the training time (basically feature selection is a machine learning technique that involve removing unecessary features from the feature space that could literally reduce the performance of our ML model).
- Describe some feature selection method: `Filter method` each feature is assing a scoring value based on a statistical analysis (pmi, correlation, etc),then are finally ranked. The features are then either added or removed from the feature space while measuring the performance of the ml model. `Wrapper method` a subset of features is selected from the feature space, using a search algorithm  and each subset obtained is compared with others based on model performance (`forward` and `backward` recursive elimination). `Embeded method` learn which features best fits a model while building the model (regularization techniques: `Lasso`, `Ridge` and `ElasticNet` regression).
- Recursive forward feature selection and backward feature selection: in `RFF` selection method, we start with no features and we incrementally add features to the model that improves model performance (conversely to the `RBF` selection method which can only be used if number of data point `N>p` where `p` is the number of features).

#### Representation learning (Rlr)

- What is representation learning? Why is it useful?:  Representation learning is concerned with machine learning algorithm that learn useful representations from the data. It help extract useful latent features in a subspace that can further be used by classifiers to perform classification.
- What is the relation between Representation Learning and Deep Learning?: deep learning can be consider as Rlr because the dl models encode useful information which are projected  into a subspace for further use (transfer learning).
- What is one-shot and zero-shot learning : In `one-shot` learning each new class has only one labeled data and predictions for new classes will be done based on this single example. In `zero-shot` learning each class has no labeled data and predictions are done based on the prior knowledge that the machine learning model has of the already known classes (may be based on cosine similarities).
- What is Greedy layer wise unsupervised pretraining ?: An approach whereby  each layer is pretrained  using an unsupervised machine learning taking the ouptut of given layer  into a  smaller and simpler representation. Greedy because we optimize each piece of a solution one a layer at a time.Layer wise because the pretraining is done on a single layer at a time , unsupervised because we use an unsupervised machine learning technique.
- Purpose of unsupervised pretraining?: It act as a `initial parametrization` for dnn therefore allowing the model to reach regions considered inaccessible at the first-step. [check here for more info](https://deep-learning-study-note.readthedocs.io/en/latest/Part%203%20(Deep%20Learning%20Research)/15%20Representation%20Learning/15.1%20Gready%20Layer%20Wise%20Unsupervised%20Pretraining.html)

#### Support Vector Machine (SVM)

- What is a p dimensional hyperplane? : A hyperplane is a p-1 dimensional flat affine subspace. For example a 2 dimensional hyperplane is a flat line (1-d affine subspace).

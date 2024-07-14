1. In [this](https://www.youtube.com/watch?v=sguol03tfWo) video there's a smooth description of how the Bayes theorem can be simply used to describe the maximum likelihood estimation.
2. The main idea in classification problems is that we want to determine the class to $C$ to which a given point belongs to ( $P(w|x)$ ).
3. As such we can use the Bayes theorem which states that: $P(w|x)= \frac{P(x|w)\times P(w)}{P(x)}$
4. The best way to solve this problem is to assume $P(x|w)$~ $N(\mu,\sigma)$ meaning the likelihood follows a normal distribution of mean ($\mu$) and standard deviation $\sigma$ which we have to determine.
5. Intuitively each data point is drawn from a normal distribution (so $x_{k}$~ $N$($\mu,\sigma$)) and the idea is to find a joint Distribution for the data generating process.
6.  Formular for Gaussian distribution : $\frac{1}{\sqrt{2\pi\sigma}}e^{-(x-\mu)^{2}}/2\sigma^{2}$ (so we want to estimate $\mu$ and $\sigma$)
7.  To get joint distribution of the entire dataset $D$, we can simply multiply each Gaussian of the points $\prod\frac{1}{\sqrt{2\pi\sigma}}e^{-(x-\mu)^{2}}/2\sigma^{2}$
8.  Now we aim to find the argmax of P(w|D) (finding the optimal $\mu$ and $\sigma$. But the argmax can only apply if the function is `concave`, which is not the case with a Gaussian. As such we use the `log` to transform it to a concave fonction. Meaning that we instead determine argmax on the log of the Gaussian function.
9.  By transforming into a log-likelihood function, we can then estimate the parameters of the data generating process simply.

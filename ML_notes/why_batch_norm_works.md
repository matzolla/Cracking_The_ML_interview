So i was having a look at this [link](https://www.youtube.com/watch?v=nUUqwaxLnWs), to understand exactly why batch normalization works
The basic intuition behind BatchNorm is that:
1. It avoids the phenomenom of `covariate-shift`, which is some how a shift in distribution between the early and later layers of a DeepNeural network.
2. `Covariate shift` is also a common issues in non-IID federated learning approach as clients (`edge devices` for example),have differences in data distribution.
3. To overcome this problem, batchnorm layers computes the running mean and standard deviation of early and later layer, to make sure that their respective weights, even if they are modified during the training process, remain constrained arround 

<h1 align="left">Bayesian search of hyperparameters in K nearest neighbor algorithm</h1>
<h2 align="center">  
  
  ## Goal 
  Utilizing Bayesian optimization to effeciently sample possible combinations of hyperparameters to make learning models perform better with suitable hyperparameters.  
  
  ## Introduction
  
Learning models with suitable hyperparameters is critical for the performance of models. However, we usually select hyperparameters manually and empirically. In order to sufficiently choose the combination of hyperparameters (maybe continous or discrete), which deepens the exploration for the relationship between hyperparameters and overall perforamance, one of the possible way is to utilize the gaussian process model to explore the "dark side" (not well known region, a.k.a high covariance part) in the relationship and sample combination which benefits our understanding the most.

  
  
  ## Description
I implemented Bayesian optimization algorithm with gaussian model to sample the possible combinations of hyperparameters in KNN model. The dataset was created randomly with 5 clusters with 2D feature (a.k.a number of features is two), which were not disclosed in the real scenario in training process. I randomly sampled 50 combinations of hyperparameters to make the gaussian model efficienly simulate the relationship between hyperparameters and overall performance of the KNN model. By simulation with Bayesian optimization (maximizing the posterior probility), I got the relationship between hyperparameters and model performace, instead of training models with various combinations of hyperparameters, which is time-comsuming.
<p align="center">
<img src="https://github.com/ychuang1234/Baysiean-search-of-hyperparamter-in-K-nearest-neighbor-algorithm/blob/4b4599a8212150995757ed98aa7516026fa60d1f/result.jpg" width="80%"></p>



## When to use ?

### Model with hyperparameters

- In Deep learning model: filter size, feature number, and depth of the model 
- In Graph convolution model: graph cut cutoff (in pooling stage)
  
### Not enough background knowledge in data
 - Let BO to explore the unknown relationship first to provide some useful insight.


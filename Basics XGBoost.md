## XGBoost
### XGBoost (which stands for eXtreme Gradient Boosting) is an especialy efficent implimentation of gradient boosting.
### XGBoost is a very powerful tool for classification and regression.

## Libraries
    library(xgboost) # for xgboost
    library(tidyverse) # general utility functions
## What is XGBoost ? Why is it so good ?
### XGBoost (Extreme Gradient Boosting) is an optimized distributed gradient boosting library. Yes, it uses gradient boosting (GBM) framework at core. Yet, does better than GBM framework alone. XGBoost was ### created by Tianqi Chen, PhD Student, University of Washington. It is used for supervised ML problems.  Let's look at what makes it so good:

    Parallel Computing: It is enabled with parallel processing (using OpenMP); 
    when you run xgboost, by default, it would use all the cores of your laptop/machine.
    Regularization: I believe this is the biggest advantage of xgboost. GBM has no provision for regularization. 
    Regularization is a technique used to avoid overfitting in linear and tree-based models.
    Enabled Cross Validation: In R, we usually use external packages such as caret and mlr to obtain CV results. 
    But, xgboost is enabled with internal CV function (we'll see below).
    Missing Values: XGBoost is designed to handle missing values internally. 
    The missing values are treated in such a manner that if there exists any trend in missing values, it is captured by the model.
    Flexibility: In addition to regression, classification, and ranking problems, it supports user-defined objective functions also. 
    An objective function is used to measure the performance of the model given a certain set of parameters. 
    Furthermore, it supports user defined evaluation metrics as well.
    Availability: Currently, it is available for programming languages such as R, Python, Java, Julia, and Scala.
    Save and Reload: XGBoost gives us a feature to save our data matrix and model and reload it later. 
    Suppose, we have a large data set, we can simply save the model and use it in future instead of wasting time redoing the computation.
    Tree Pruning: Unlike GBM, where tree pruning stops once a negative loss is encountered, 
    XGBoost grows the tree upto max_depth and then prune backward until the improvement in loss function is below a 
    threshold.

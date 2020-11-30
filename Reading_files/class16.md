## Linear Regression

- _Scikit-learn_ is a powerful Python module for machine learning. It contains function for regression, classification, clustering, model selection and dimensionality reduction.

    - __sklearn.linear_model__ module which contains “methods intended for regression in which the target value is expected to be a linear combination of the input variables”.


- Important functions to keep in mind while fitting a linear regression model  are:

    1. lm.fit() -> fits a linear model

    2. lm.predict() -> Predict Y using the linear model with estimated coefficients

    3. lm.score() -> Returns the coefficient of determination (R^2). A measure of how well observed outcomes are replicated by the model, as the proportion of total variation of outcomes explained by the model.

- In practice you wont implement linear regression on the entire data set, you will have to split the data sets into training and test data sets. So that you train your model on training data and see how well it performed on test data.

- Residual plots are a good way to visualize the errors in your data. If you have done a good job then your data should be randomly scattered around line zero. If you see structure in your data, that means your model is not capturing some thing. Maye be there is a interaction between 2 variables that you are not considering, or may be you are measuring time dependent data. If you get some structure in your data, you should go back to your model and check whether you are doing a good job with your parameters.








[<===BACK](../README.md)

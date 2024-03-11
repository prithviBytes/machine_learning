# Multiple Linear Regression

## Introduction

In this lesson, we'll learn about **_Multiple Linear Regression_**, a powerful tool for making predictions when there are multiple features that can be used to predict a target variable.

## Objectives

You will be able to:

- Understand and explain what Multiple Linear Regression is
- Understand and explain the mathematics behind Multiple Linear Regression
- Understand how to use Multiple Linear Regression to make predictions on a dataset

## What is Multiple Linear Regression?

In the previous section, we learned about simple linear regression, which is a method for making predictions about a target variable based on a single feature. However, in the real world, we often have more than one feature that we can use to make predictions. For example, if we were trying to predict the price of a house, we wouldn't just use the square footage of the house--we'd also want to know how many bedrooms and bathrooms it has, how big the lot is, and so on. 

When we have more than one feature that we can use to make predictions, we use **_Multiple Linear Regression_**. Multiple Linear Regression is a straightforward extension of simple linear regression, and the mathematics behind it is very similar. The only difference is that instead of having a single feature to use to make predictions, we have multiple features.

## The Mathematics Behind Multiple Linear Regression

The mathematics behind multiple linear regression is very similar to the mathematics behind simple linear regression. The only difference is that instead of having a single feature, we have multiple features.

The formula for the line in simple linear regression is:

$$y = mx + b$$

In multiple linear regression, the formula is:

$$y = m_1x_1 + m_2x_2 + m_3x_3 + ... + b$$

In this formula, $m_1$, $m_2$, $m_3$, etc. are the coefficients for each feature, and $b$ is the y-intercept.

## Assumptions of Multiple Linear Regression

The assumptions of multiple linear regression are the same as the assumptions for simple linear regression. The only difference is that we have to check these assumptions for each feature. The assumptions are:

1. **Linearity**: The relationship between the features and the target variable is linear.
2. **Homoscedasticity**(Normal Variance): The variance of the errors is consistent across all levels of the target variable.
3. **Multivariate Normality**: The errors are normally distributed.
4. **Independence**: The features are independent of each other.
5. **Lack of Multicollinearity**: The features are not highly correlated with each other.
6. **Outliers**: There are no significant outliers in the data.


## Dummy Variables

One important thing to note is that if we have categorical variables, we need to convert them into **_dummy variables_**. A dummy variable is a binary variable that represents a category. For example, if we had a dataset of houses and one of the features was "neighborhood", we would need to convert the "neighborhood" feature into dummy variables. If there were 5 neighborhoods in the dataset, we would create 5 dummy variables, one for each neighborhood. Each dummy variable would be 1 if the house was in that neighborhood, and 0 if it wasn't.

### Dummy Variable Trap

One thing to note is that if we have $n$ dummy variables, we only need $n-1$ dummy variables. This is because if we have $n$ dummy variables, we can infer the value of the $n$th dummy variable from the other $n-1$ dummy variables. This is known as the **_dummy variable trap_**.

## P-value

The p-value is a measure of how likely it is that the coefficient for a feature is actually zero. If the p-value for a feature is less than 0.05, we can conclude that the feature is statistically significant and has a non-zero coefficient. If the p-value is greater than 0.05, we can conclude that the feature is not statistically significant and has a coefficient of zero.


## Building a Model

5 methods to build a model

1. **All in**: Put all the variables into the model.

2. **Backward Elimination**: Start with all the variables and remove the least significant variable at each step until the model's performance stops improving.

- Select a significance level to stay in the model (e.g. SL = 0.05)
- Fit the full model with all possible predictors
- Consider the predictor with the highest P-value. If P > SL, go to step 3, otherwise, the model is ready.
- Remove the predictor
- Fit the model without this variable

3. **Forward Selection**: Start with no variables and add the most significant variable at each step until the model's performance stops improving.

- Select a significance level to enter the model (e.g. SL = 0.05)
- Fit all simple regression models $y ~ x_n$ and select the one with the lowest P-value
- Keep this variable and fit all possible models with one extra predictor added to the one(s) you already have
- Consider the predictor with the lowest P-value. If P < SL, go to step 3, otherwise, the model is ready.

4. **Bidirectional Elimination**: Perform a combination of the forward and backward elimination processes.

- Select a significance level to enter and to stay in the model (e.g. SLENTER = 0.05, SLSTAY = 0.05)
- Perform the next step of forward selection (new variables must have P < SLENTER to enter)
- Perform all steps of backward elimination (old variables must have P < SLSTAY to stay)
- No new variables can enter and no old variables can exit

5. **All Possible Models (Score Comparison)**: Select the model with the best score.

- Select a criterion of goodness of fit (e.g. Akaike criterion)
- Construct all possible regression models: $2^N - 1$ total combinations
- Select the one with the best criterion


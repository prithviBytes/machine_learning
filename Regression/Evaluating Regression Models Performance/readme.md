## R Squared

R-squared, or the coefficient of determination, is a measure used to understand how well a regression model fits the data. It tells us the proportion of the variance in the dependent variable that is predictable from the independent variable(s).

In simpler terms, R-squared answers the question: "How well does our regression line explain the variation in the data?"

## Formula

The formula to calculate R-squared is:

R-squared = 1 - (SSR/SST)

Where:

SSR = Sum of Squared Residuals
SST = Sum of Squared Total

## Interpretation

R-squared is always between 0 and 100%. An R-squared of 100% means that all movements of a dependent variable are completely explained by movements in the independent variable(s) you are interested in. In general, the higher the R-squared, the better the model fits your data.

## Example

Let's say we have a dataset with two variables, X and Y. We fit a regression model to the data and calculate the R-squared value. If the R-squared value is 0.80, it means that 80% of the variation in the dependent variable (Y) is predictable from the independent variable (X).


## Adjusted R Squared

Adjusted R-squared is a modified version of R-squared that has been adjusted for the number of predictors in the model. The adjusted R-squared increases only if the new term improves the model more than would be expected by chance.

The adjusted R-squared is a better measure of the goodness of fit of a regression model, as it accounts for the number of predictors in the model.

## Formula

The formula to calculate Adjusted R-squared is:

Adjusted R-squared = 1 - [(1-R^2)(n-1)/(n-p-1)]

Where:

R^2 = R-squared
n = number of observations
p = number of predictors

## Problem with R Squared

R-squared has a major limitation: it increases as the number of predictors in the model increases, even if the predictors are only weakly associated with the dependent variable. This is where adjusted R-squared comes in. It penalizes the addition of unnecessary predictors to the model, and only increases if the new predictor enhances the model's performance.
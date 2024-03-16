# Logistic Regression

Logistic regression is a statistical method used for binary classification, which means it predicts the probability that an instance belongs to a particular class. It's called "logistic" because it's based on the logistic function, also known as the sigmoid function.

Here's a quick rundown:

Binary Classification: Logistic regression predicts the probability that an instance belongs to one of two classes, usually represented as 0 or 1.

Sigmoid Function: The logistic regression model applies the sigmoid function to a linear combination of input features and their associated weights. The sigmoid function transforms any input into a value between 0 and 1, which can be interpreted as a probability.

Decision Boundary: Based on the calculated probabilities, logistic regression assigns instances to the class with the highest probability. It does this by setting a threshold (usually 0.5), above which instances are classified as belonging to one class and below which they are classified as belonging to the other class.

Training: The model's parameters (weights) are optimized during training using techniques like maximum likelihood estimation or gradient descent to minimize the difference between predicted probabilities and actual class labels.

In simple terms, logistic regression is like fitting a curve to separate two classes, with the curve representing the probability of belonging to one class. If the probability is above a certain threshold, we classify it as one class; otherwise, we classify it as the other class.

## Maximum Likelihood Estimation

Maximum likelihood estimation (MLE) is a method used to estimate the parameters of a statistical model. It's based on the principle that the best estimates of the model's parameters are those that maximize the likelihood of the observed data.
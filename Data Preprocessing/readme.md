# Data Pre-processing

## What is Data Pre-processing?

Data preprocessing is a crucial step in machine learning where raw data is transformed into a clean and structured format that can be used for analysis. It involves various techniques such as data cleaning, data transformation, and data normalization to ensure the data is suitable for training machine learning models

## Training set and Test set

The training set is a dataset used to train a model. The test set is a dataset used to measure how well the model performs at making predictions on that test set.

## Feature Scaling

Feature scaling is a method used to standardize the range of independent variables or features of data. In data processing, it is also known as data normalization and is generally performed during the data preprocessing step.

### Why do we need Feature Scaling?

- It helps to normalize the data within a particular range.
- It helps to speed up the training process.
- It helps to prevent the algorithm from getting stuck in local optima.

### Normalization with example

Normalization is a scaling technique in which values are shifted and rescaled so that they end up ranging between 0 and 1. It is also known as Min-Max scaling.

#### Formula for Normalization

```
Xnorm = (X - Xmin) / (Xmax - Xmin)
```

#### Example

```
X = [1, 2, 3, 4, 5]
Xmax = 5
Xmin = 1
Xnorm = [(1-1)/(5-1), (2-1)/(5-1), (3-1)/(5-1), (4-1)/(5-1), (5-1)/(5-1)]
Xnorm = [0, 0.25, 0.5, 0.75, 1]
```

#### Why do we Normalize?

- It is easier to optimize the cost function.
- It prevents the algorithm from getting stuck in local optima.
- It speeds up the training process.

### Standardization with example

Standardization is a scaling technique where the values are centered around the mean with a unit standard deviation. This means that the mean of the attribute becomes zero and the resultant distribution has a unit standard deviation.

#### Formula for Standardization

```
Xstd = (X - mean) / standard deviation
```

#### Example

```
X = [1, 2, 3, 4, 5]
mean = 3
standard deviation = 1.41
Xstd = [(1-3)/1.41, (2-3)/1.41, (3-3)/1.41, (4-3)/1.41, (5-3)/1.41]
Xstd = [-1.41, -0.71, 0, 0.71, 1.41]
```

#### Why do we Standardize?

- It makes the algorithm converge faster.
- It prevents the algorithm from getting stuck in local optima.
- It makes the algorithm less sensitive to the scale of features.


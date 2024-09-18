# Time-series-classification-from-scratch
### Introduction
This project shows how to do time-series classification from scratch, starting from raw CSV time-series files on disk. We demonstrate the workflow on the FordA dataset from the UCR/UEA archive.

### Dataset description
The dataset we are using here is called FordA. The data comes from the UCR archive. The dataset contains 3601 training instances and another 1320 testing instances. Each timeseries corresponds to a measurement of engine noise captured by a motor sensor. For this task, the goal is to automatically detect the presence of a specific issue with the engine. The problem is a balanced binary classification task.

### Standardize the data
Our timeseries are already in a single length (500). However, their values are usually in various ranges. This is not ideal for a neural network; in general we should seek to make the input values normalized. For this specific dataset, the data is already z-normalized: each timeseries sample has a mean equal to zero and a standard deviation equal to one. This type of normalization is very common for timeseries classification problems.

### Conclusion:
The model achieves optimal performance after 200 epochs, with balanced training and validation accuracies (0.97). Further training leads to overfitting, indicating 200 epochs as the optimal stopping point.

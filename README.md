# Flight Search Caching

## Problem Statment
Given flight search data, which contains information like fare, departure date, sector(arrival-destination), timestamp, we aim to understand and predict when will the next search hit come, and will the price fare change with the next hit. This is done so as to utilise pre-emptive caching for best search performance. 

## Methodology
We prepare our data according to the data required in survival analysis, i.e. (_Survival Time, Status_). Then we begin to try out several variations of survival models (CoxPH Survival Model, Survival Random Forest, Survival SVM, etc.)

## Benchamarking
We create a custom metric function that is used for evaluating how precise our predictions are. From the training data, we select a probability threshold (from death function) for which the error between actual and predicted is minimum. Based on this threshold we calculate the error between our model predictions and the ground truth.

### Note 
Actual data and results cannot be published so as to maintain compliance with Ixigo's policies.

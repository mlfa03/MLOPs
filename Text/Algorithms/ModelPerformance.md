# Model Performance 

How to evaluate models?

## Classification Models 

### Accuracy 
Accuracy score in machine learning is an evaluation metric that measures the number of correct predictions made by a model in relation to the total number of predictions made. We calculate it by dividing the number of correct predictions by the total number of predictions. 

It works well only if there are equal number of samples belonging to each class.

### Precision
It is the number of correct positive results divided by the number of positive results predicted by the classifier.

### Recall 
 It is the number of correct positive results divided by the number of all relevant samples (all samples that should have been identified as positive).

### f1-Score 
F1 Score is the Harmonic Mean between precision and recall. The range for F1 Score is [0, 1]. It tells you how precise your classifier is (how many instances it classifies correctly), as well as how robust it is (it does not miss a significant number of instances).
High precision but lower recall, gives you an extremely accurate, but it then misses a large number of instances that are difficult to classify. The greater the F1 Score, the better is the performance of our model.


### Sensitivity (TPR)
True Positive Rate is defined as TP/ (FN+TP). True Positive Rate corresponds to the proportion of positive data points that are correctly considered as positive, with respect to all positive data points.
It means the models ability to correctly classify the samples. 
**Higher sensitivity you have fewer false negatives**

### Specificity (TNR)
rue Negative Rate is defined as TN / (FP+TN). TNR corresponds to the proportion of negative data points that are correctly considered as negative, with respect to all negative data points.
Classifier's ability to correctly classify legitimate examples. 
**Higher specificity you have fewer false positives**

We can balance specificity and sensitivity by changing our decision threshold. 

### False Positive Rate 
is defined as FP / (FP+TN). False Positive Rate corresponds to the proportion of negative data points that are mistakenly considered as positive, with respect to all negative data points.



### AUC (Area Under Curve) 
It is used for binary classification problem. AUC of a classifier is equal to the probability that the classifier will rank a randomly chosen positive example higher than a randomly chosen negative example.

### ROC (Receiver Operator Curve)
Plot of how the specificity and sensitivity change as the decision threshold changes. The area under the curve is the probability that a randomly
chosen posititive example will have a higher prediction probability of being positive than a randomly chosen negative. 

## Regression Models 

### MAE (Mean Absolute Error) 


### MSE (Mean Squared Error)
Mean Squared Error(MSE) is quite similar to Mean Absolute Error, the only difference being that MSE takes the average of the square of the difference between the original values and the predicted values. The advantage of MSE being that it is easier to compute the gradient, whereas Mean Absolute Error requires complicated linear programming tools to compute the gradient. As, we take square of the error, the effect of larger errors become more pronounced then smaller error, hence the model can now focus more on the larger errors.

### RMSE (Root Mean Squared Error) 


### R2 

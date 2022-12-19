## Linear Regression

### Glossary 
 * **p-value**: probability of finding a particular result, or a greater result, given a null hypothesis being true. 
 * **confidence interval**: The possible range of an unknown value. Often comes with some degree probability (ex. 95% confidence interval)
 * **R squared**: The percent of variance in the dependent variable explained by the independent variable. 
 * **Variance inflation factor**: a measure of collinearity in a regression model. Equals 1 --> no collinearity. , Between one e 0.5 --> some collinearity, lower than 0.5 --> severe collinearity
 * **Feature interaction**: features that are multiplied by one another in order to express relationships that can't be represented by adding the independent variable terms together. 


### Main concepts 
* Algorithm that is used to predict a continuous target variable. 
* A linear regression model predicts the target as a weighted sum of the feature inputs. 



### How does it work?
![image](https://user-images.githubusercontent.com/39881974/201339267-9b4a0de5-678e-4dc8-8f29-5e5d277d013d.png)

For simple linear regression, where there is one independent variable (feature) and one dependent variable (target) the algorithm can be represented by the following equation:

![image](https://user-images.githubusercontent.com/39881974/208433471-b758678e-dba6-47d9-bc0c-0319d2ddf74d.png)

* The predicted outcome of an instance is a weighted sum of its p features
* The betas represent the learned feature weights or coefficients
* The first weight in the sum (β0) is called the intercept and is not multiplied with a feature
* The epsilon (ϵ) is the error we still make, i.e. the difference between the prediction and the actual outcome
* These errors are assumed to follow a Gaussian distribution, which means that we make errors in both negative and positive directions and make many small errors and few large errors.

The ordinary least squares method is usually used to find the weights that minimize the squared differences between the actual and the estimated outcomes:

![image](https://user-images.githubusercontent.com/39881974/208433795-f889e73f-ebbf-4cb2-bc0f-c0e3db1693a6.png)

An important measurement for interpreting linear models is the R-squared measurement. R-squared tells you how much of the total variance of your target outcome is explained by the model. The higher R-squared, the better your model explains the data.

![image](https://user-images.githubusercontent.com/39881974/208435922-aae50f8f-a4a0-4bd8-a888-ced63deb614e.png)

There is a catch, because R-squared increases with the number of features in the model, even if they do not contain any information about the target value at all. Therefore, it is better to use the adjusted R-squared, which accounts for the number of features used in the model. Its calculation is:

![image](https://user-images.githubusercontent.com/39881974/208436275-5489a7ef-08d3-4172-ae06-c224224209b3.png)

**Feature Importance**
The importance of a feature in a linear regression model can be measured by the absolute value of its t-statistic. The t-statistic is the estimated weight scaled with its standard error.

![image](https://user-images.githubusercontent.com/39881974/208436496-85dd5717-3af7-45dd-98c8-79ee1d2445e6.png)

The importance of a feature increases with increasing weight. This makes sense. The more variance the estimated weight has (= the less certain we are about the correct value), the less important the feature is. This also makes sense.


### Recommendations:
* Performs very well on linearly separable data.
* Not good for datasets with too many outliers, it is not robust to this condition 
* Can only be used to solve regression-based problems.
* **Linearity**: There must be a linear relationship between the dependent and independent variables. Linearity leads to interpretable models. Linear effects are easy to quantify and describe. They are additive, so it is easy to separate the effects. If you suspect feature interactions or a nonlinear association of a feature with the target value, you can add interaction terms or use regression splines.
* **Normality**: It is assumed that the target outcome given the features follows a normal distribution. If this assumption is violated, the estimated confidence intervals of the feature weights are invalid.
* **Homoscedasticity (constant variance)**: The variance of the error terms is assumed to be constant over the entire feature space.
* **Absence of multicollinearity**: There must be no correlation between features, this messes up with the estimation of the weights. This happens because the feature effects are additive and it becomes indeterminable to which of the correlated features to attribute the effects.
* **Independence**: It is assumed that each instance is independent of any other instance. 
* The algorithm assumes that training data is randomly sampled.
* **Fixed features**: The input features are considered “fixed”. Fixed means that they are treated as “given constants” and not as statistical variables. This implies that they are free of measurement errors. This is a rather unrealistic assumption. Without that assumption, however, you would have to fit very complex measurement error models that account for the measurement errors of your input features. And usually you do not want to do that.
* Best suited to regression-based problems where the relationships in the data are both linear and simple.

Some additional points: 

* Highly interpretable and fast to train.
* Very simplistic and so it doesn't model the complexities found in real-world data well.
*  Prone to overfitting.

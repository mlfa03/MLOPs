## Logistic Regression

### Main Concepts

* Logistic regression is essentially linear regression moulded to fit a classification problem. 
* Instead of fitting a straight line, logistic regression applies the logistic function to squeeze the output of a linear equation between 0 and 1. 
* The result is an S-shaped curve rather than a straight line through the data points
* Does not require a linear relationship between predictions and predictors

**Linear Regression x Logistic Regression**
* A linear model does not output probabilities, but it treats the classes as numbers (0 and 1) and fits the best hyperplane (for a single feature, it is a line) that minimizes the distances between the points and the hyperplane. So it simply interpolates between the points, and you cannot interpret it as probabilities.
* A linear model also extrapolates and gives you values below zero and above one. This is a good sign that there might be a smarter approach to classification.
* Since the predicted outcome is not a probability, but a linear interpolation between points, there is no meaningful threshold at which you can distinguish one class from the other.
* Linear models do not extend to classification problems with multiple classes. You would have to start labeling the next class with 2, then 3, and so on. The classes might not have any meaningful order, but the linear model would force a weird structure on the relationship between the features and your class predictions. The higher the value of a feature with a positive weight, the more it contributes to the prediction of a class with a higher number, even if classes that happen to get a similar number are not closer than other classes.

#### How does it work?

* Instead of fitting a straight line or hyperplane, the logistic regression model uses the logistic function to squeeze the output of a linear equation between 0 and 1. This function is the Sigmoid function: 

![image](https://user-images.githubusercontent.com/39881974/200902384-7952c15d-74e7-44d6-bffb-4a39a04f8784.png)


* X is a matrix containing input features and theta is the randomly initialized values that will be updated in the algorithm. 

![image](https://user-images.githubusercontent.com/39881974/200902342-18b4aacd-0a78-4651-ac8b-63573de2c112.png)

 
* A cost function gives the measure of how far the predicted output is from the original labels (‘y’ vector). ‘m’ is the number of training data. 

![image](https://user-images.githubusercontent.com/39881974/200902235-6df9690c-85dc-447e-ae44-44075edbb7bf.png)

* Theta values are updated to minimize the cost function. 

![image](https://user-images.githubusercontent.com/39881974/200902301-d9499aa2-2ed5-4a31-8136-5bac56d759f4.png)

**Interpretation**
The interpretation of the weights in logistic regression differs from the interpretation of the weights in linear regression, since the outcome in logistic regression is a probability between 0 and 1. The weights do not influence the probability linearly any longer. The weighted sum is transformed by the logistic function to a probability. Therefore we need to reformulate the equation for the interpretation so that only the linear term is on the right side of the formula.

![image](https://user-images.githubusercontent.com/39881974/208457669-ac322dac-98e4-4555-9421-7fa461dcf7f7.png)

We call the term in the **ln() function “odds” (probability of event divided by probability of no event) and wrapped in the logarithm it is called log odds.**
* **Numerical feature**: If you increase the value of feature xj by one unit, the estimated odds change by a factor of exp(βj)
* **Binary categorical feature**: One of the two values of the feature is the reference category (in some languages, the one encoded in 0). Changing the feature xj from the reference category to the other category changes the estimated odds by a factor of exp(βj).
* **Categorical feature with more than two categories**: One solution to deal with multiple categories is one-hot-encoding, meaning that each category has its own column. You only need L-1 columns for a categorical feature with L categories, otherwise it is over-parameterized. The L-th category is then the reference category. You can use any other encoding that can be used in linear regression. The interpretation for each category then is equivalent to the interpretation of binary features.
* **Intercept β0**: When all numerical features are zero and the categorical features are at the reference category, the estimated odds are exp(β0). The interpretation of the intercept weight is usually not relevant.

### Recommended use
* This algorithm can only be used to solve classification problems.
* There must be a linear relationship between features and the target variable.
* The number of observations must be larger than the number of features.
* Best suited to classification problems where the relationships in the data are both linear and simple.
* Many of the pros and cons of the linear regression model also apply to the logistic regression model. Logistic regression has been widely used by many different people, but it struggles with its restrictive expressiveness (e.g. interactions must be added manually) and other models may have better predictive performance.
* The interpretation is more difficult because the interpretation of the weights is multiplicative and not additive.
* Logistic regression can suffer from complete separation. If there is a feature that would perfectly separate the two classes, the logistic regression model can no longer be trained. This is because the weight for that feature would not converge, because the optimal weight would be infinite.

## Logistic Regression

### Main Concepts

* Logistic regression is essentially linear regression moulded to fit a classification problem. 
* Instead of fitting a straight line, logistic regression applies the logistic function to squeeze the output of a linear equation between 0 and 1. 
* The result is an S-shaped curve rather than a straight line through the data points
* Does not require a linear relationship between predictions and predictors

#### How does it work?

* Sigmoid function to predict output.

![image](https://user-images.githubusercontent.com/39881974/200902384-7952c15d-74e7-44d6-bffb-4a39a04f8784.png)


* X is a matrix containing input features and theta is the randomly initialized values that will be updated in the algorithm. 

![image](https://user-images.githubusercontent.com/39881974/200902342-18b4aacd-0a78-4651-ac8b-63573de2c112.png)

 
* A cost function gives the measure of how far the predicted output is from the original labels (‘y’ vector). ‘m’ is the number of training data. 

![image](https://user-images.githubusercontent.com/39881974/200902235-6df9690c-85dc-447e-ae44-44075edbb7bf.png)

* Theta values are updated to minimize the cost function. 

![image](https://user-images.githubusercontent.com/39881974/200902301-d9499aa2-2ed5-4a31-8136-5bac56d759f4.png)

### Recommended use
* This algorithm can only be used to solve classification problems.
* There must be a linear relationship between features and the target variable.
* The number of observations must be larger than the number of features.
* Best suited to classification problems where the relationships in the data are both linear and simple.

## Linear Regression

### Main concepts 
* Algorithm that is used to predict a continuous target variable. 



### How does it work?
![image](https://user-images.githubusercontent.com/39881974/201339267-9b4a0de5-678e-4dc8-8f29-5e5d277d013d.png)

For simple linear regression, where there is one independent variable (feature) and one dependent variable (target) the algorithm can be represented by the following equation:

*y = ax + b*


### Recommended use
* Performs very well on linearly separable data.
* Not good for datasets with too many outliers, it is not robust to this condition 
* Can only be used to solve regression-based problems.
* There must be a linear relationship between the dependent and independent variables.
* Residuals must form a normal distribution.
* There must be no correlation between features.
* The algorithm assumes that training data is randomly sampled.
* Best suited to regression-based problems where the relationships in the data are both linear and simple.

Some additional points: 

* Highly interpretable and fast to train.
* Very simplistic and so it doesn't model the complexities found in real-world data well.
*  Prone to overfitting.

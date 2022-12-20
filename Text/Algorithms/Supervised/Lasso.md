## Lasso Regression

**[back to index](https://github.com/mlfa03/MLOPs/blob/main/README.md)**

Lasso is an automatic and convenient way to introduce sparsity into the linear regression model. Lasso stands for “least absolute shrinkage and selection operator” and, when applied in a linear regression model, performs feature selection and regularization of the selected feature weights. 

### Main concepts 

**Regularization**

* Regularization is an important concept that is used to avoid overfitting of the data, especially when the trained and test data are much varying.
* Regularization is implemented by adding a “penalty” term to the best fit derived from the trained data, to achieve a lesser variance with the t tested data and also restricts the influence of predictor variables over the output variable by compressing their coefficients.
* We keep the same number of features but reduce the magnitude of the coefficients. We can reduce the magnitude of the coefficients by using different types of regression techniques which uses regularization to overcome this problem. 

**L1 Regularization**

* If a regression model uses the L1 Regularization technique, then it is called Lasso Regression. If it used the L2 regularization technique, it’s called Ridge Regression
* L1 regularization adds a penalty that is equal to the absolute value of the magnitude of the coefficient. 
* This regularization type can result in sparse models with few coefficients. 
* Some coefficients might become zero and get eliminated from the model. 
* Larger penalties result in coefficient values that are closer to zero (ideal for producing simpler models). 
* On the other hand, L2 regularization does not result in any elimination of sparse models or coefficients. Thus, Lasso Regression is easier to interpret as compared to the Ridge. 

### How does it work?

**Residual Sum of Squares + λ * (Sum of the absolute value of the magnitude of coefficients)**

Where,

    * λ denotes the amount of shrinkage.
    * λ = 0 implies all features are considered and it is equivalent to the linear regression where only the residual sum of squares is considered to build a predictive model
    * λ = ∞ implies no feature is considered i.e, as λ closes to infinity it eliminates more and more features
    * The bias increases with increase in λ
    * variance increases with decrease in λ

Considering the minimization problem that the weights optimize:

![image](https://user-images.githubusercontent.com/39881974/208437938-9d5a9d1f-5d26-4496-8062-6fa3ee2c568f.png)

* The term **||β||1**, the L1-norm of the feature vector, leads to a penalization of large weights. Since the L1-norm is used, many of the weights receive an estimate of 0 and the others are shrunk. 
* The parameter **lambda (λ)** controls the strength of the regularizing effect and is usually tuned by cross-validation. Especially when lambda is large, many weights become 0. The feature weights can be visualized as a function of the penalty term lambda. 

If you see the penalization term as a tuning parameter, then you can find the lambda that minimizes the model error with cross-validation. You can also consider lambda as a parameter to control the interpretability of the model. The larger the penalization, the fewer features are present in the model (because their weights are zero) and the better the model can be interpreted.

### Recommended use

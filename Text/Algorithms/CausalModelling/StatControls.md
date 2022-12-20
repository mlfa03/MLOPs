## Experimental Design and Statistical Controls 

**[back to index](https://github.com/mlfa03/MLOPs/blob/main/README.md)**

### Covariate (control variable)
* Technically, a covariate is a variable that is of no direct interest to the researcher, but one that may have an affect on the outcome (the dependent variable). Results of a study can be made more accurate by controlling for the variation in the covariate. So, a covariate is in fact, a type of control variable.
* 

### ANCOVA
Analysis of covariance is used to test the main and interaction effects of categorical variables on a continuous dependent variable, controlling for the effects of selected other continuous variables, which co-vary with the dependent. The control variables are called the "covariates."

ANCOVA is used for several purposes:

    * In experimental designs, to control for factors which cannot be randomized but which can be measured on an interval scale.
    * In observational designs, to remove the effects of variables which modify the relationship of the categorical independents to the interval dependent.
    * In regression models, to fit regressions where there are both categorical and interval independents. (This third purpose has become displaced by logistic regression and other methods.
 
 
### f-test 
* The F-test of significance is used to test each main and interaction effect, for the case of a single interval dependent and multiple (>2) groups formed by a categorical independent. 
* F is between-groups variance divided by within-groups variance. If the computed p-value is small, then significant relationships exist.

![image](https://user-images.githubusercontent.com/39881974/208311269-bad34101-ed58-49ab-8281-984fcfa824c1.png)

Step by step:
1. State the null hypothesis and the alternate hypothesis.
2, Calculate the F value. The F Value is calculated using the formula F = (SSE1 – SSE2 / m) / SSE2 / n-k, where SSE = residual sum of squares, m = number of restrictions and k = number of independent variables.
3. Find the F Statistic (the critical value for this test). The F statistic formula is:
F Statistic = variance of the group means / mean of the within group variances.
You can find the F Statistic in the F-Table.
4. Support or Reject the Null Hypothesis.

### t-test 
A t-test is an inferential statistic used to determine if there is a significant difference between the means of two groups and how they are related. T-tests are used when the data sets follow a normal distribution and have unknown variances, like the data set recorded from flipping a coin 100 times.

* A t-test is an inferential statistic used to determine if there is a statistically significant difference between the means of two variables.
* The t-test is a test used for hypothesis testing in statistics.
* Calculating a t-test requires three fundamental data values including the difference between the mean values from each data set, the standard deviation of each group, and the number of data values.
* T-tests can be dependent or independent.


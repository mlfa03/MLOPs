# Feature Processing 

### Feature Scaling 

**Why some algorithms require feature scaling?*

* Machine learning algorithms like linear regression, logistic regression, neural network, etc. that use gradient descent as an optimization technique require data to be scaled.
* The presence of feature value X in the formula will affect the step size of the gradient descent. The difference in ranges of features will cause different step sizes for each feature. To ensure that the gradient descent moves smoothly towards the minima and that the steps for gradient descent are updated at the same rate for all the features, we scale the data before feeding it to the model.
* Having features on a similar scale can help the gradient descent converge more quickly towards the minima.
* Distance algorithms like KNN, K-means, and SVM are most affected by the range of features. This is because behind the scenes they are using distances between data points to determine their similarity.

**What about tree-based algorithms?**
* Tree-based algorithms, on the other hand, are fairly insensitive to the scale of the features. 
* The decision tree splits a node on a feature that increases the homogeneity of the node. This split on a feature is not influenced by other features.
*  


### Feature Normalization 
* Normalization is a scaling technique in which values are shifted and rescaled so that they end up ranging between 0 and 1. It is also known as Min-Max scaling.
* Implement it with MinMaxScaler() from scikit-learn

### Feature Standardization 
* Standardization is another scaling technique where the values are centered around the mean with a unit standard deviation. 
* This means that the mean of the attribute becomes zero and the resultant distribution has a unit standard deviation.
* Implement it with StandardScaler() from scikit-learn 

### Normalization x Standardization? 
* **Normalization** is good to use when you know that the distribution of your data does not follow a Gaussian distribution. 
* This can be useful in algorithms that do not assume any distribution of the data like K-Nearest Neighbors and Neural Networks.
* **Standardization**, on the other hand, can be helpful in cases where the data follows a Gaussian distribution. 
* However, this does not have to be necessarily true. Also, unlike normalization, standardization does not have a bounding range. So, even if you have outliers in your data, they will not be affected by standardization.

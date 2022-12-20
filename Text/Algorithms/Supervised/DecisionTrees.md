# Decision Trees

**[back to index](https://github.com/mlfa03/MLOPs/blob/main/README.md)**

* Linear regression and logistic regression models fail in situations where the relationship between features and outcome is nonlinear or where features interact with each other. 
* Tree based models split the data multiple times according to certain cutoff values in the features. Through splitting, different subsets of the dataset are created, with each instance belonging to one subset. 
* The final subsets are called terminal or leaf nodes and the intermediate subsets are called internal nodes or split nodes. 
* To predict the outcome in each leaf node, the average outcome of the training data in this node is used. Trees can be used for classification and regression.

## Glossary
* **Decision Trees**: a tree based model which traverses examples down to leaf nodes by the properties of the examples features. 
* **CART - Classification and Regression Tree**: algorithm for constructing an approximate optimal decision tree for given examples. 
* **split point**: a pair of feature and feature value which is assigned to a node in a tree. This split point will determine which examples will go left and which examples will go right based on the feature and feature value. 
* **Gini impurity**: used as a way to determine the best split point for a given node in a classification tree. It is based on the probability of incorrectly classifying an item based on all of the items in the node. 
* **Surrogate split**: suboptimal split point reserved for examples which are missing the optimal split point feature. 
* **Boosting**: an ensemble technique which trains many weak learners sequentially , with each subsequent weak learner being trained on the previous weak learner's error. This generally reduces bias error. 
* **Bagging**: also bootstrap aggregation, a sampling technique which selects subsets of examples and/or features to train an ensemble of models. This generally reduces the variance error. 
* **Weak learner**: shallow decision trees. It generally can be an underfitting model. 

## Simple Decision Trees 
The following formula describes the relationship between the outcome y and features x.

![image](https://user-images.githubusercontent.com/39881974/208484573-3411e662-2bbc-4d85-b13e-f869e0925001.png)

Each instance falls into exactly one leaf node (=subset Rm). I{x∈Rm} is the identity function that returns 1 if x is in the subset Rm and 0 otherwise. If an instance falls into a leaf node Rl, the predicted outcome is ^y=cl, where cl is the average of all training instances in leaf node Rl.

**But where do the subsets come from?** 
* **Regression Trees**: CART takes a feature and determines which cut-off point minimizes the variance of y. The variance tells us how much the y values in a node are spread around their mean value. 
* **Classification Trees**: Gini index of the class distribution of y. The Gini index tells us how “impure” a node is, e.g. if all classes have the same frequency, the node is impure, if only one class is present, it is maximally pure. 
* **Variance and Gini index are minimized when the data points in the nodes have very similar values for y.**
* As a consequence, the best cut-off point makes the two resulting subsets as different as possible with respect to the target outcome. 
* For categorical features, the algorithm tries to create subsets by trying different groupings of categories. 
* After the best cutoff per feature has been determined, the algorithm selects the feature for splitting that would result in the best partition in terms of the variance or Gini index and adds this split to the tree. 
* The algorithm continues this search-and-split recursively in both new nodes until a stop criterion is reached. 
* **Possible stopping criteria**: minimum number of instances that have to be in a node before the split, or the minimum number of instances that have to be in a terminal node.

## Random Forest
Technique that trains many independent weak learners. This generally reduces the variance error. 

### Main concepts 

* Ensemble of decision trees.
* A percentage of the original dataset is randomly selected with replacement. 
* When splitting nodes, random subsets of features are considered.
* Predictions are combined by majority voting for classification

**Decision Tree x Random Forest**

![image](https://user-images.githubusercontent.com/39881974/200903525-2bf559c5-8231-4301-a152-c29138c94c2e.png)


### How does it work?
* The training dataset is randomly split into multiple samples based on the number of trees in the forest. The number of trees is set via a hyperparameter.
* The decision trees are trained in parallel using one of the data subsets.
* The output of all trees is evaluated and the most commonly occurring prediction is taken as the final result.

1. The root node in a decision tree is our starting point. If we were to use the root node to make predictions, it would predict the mean of the outcome of the training data. 
2. With the next split, we either subtract or add a term to this sum, depending on the next node in the path. 
3. To get to the final prediction, we have to follow the path of the data instance that we want to explain and keep adding to the formula.

![image](https://user-images.githubusercontent.com/39881974/208487085-c91118aa-fa0b-4a2e-8495-3e35899e7841.png)

4. The prediction of an individual instance is the mean of the target outcome plus the sum of all contributions of the D splits that occur between the root node and the terminal node where the instance ends up. 
5. We are not interested in the split contributions though, but in the feature contributions. A feature might be used for more than one split or not at all. 
6. We can add the contributions for each of the p features and get an interpretation of how much each feature has contributed to a prediction.

**Interpretation**
1. Starting from the root node, you go to the next nodes and the edges tell you which subsets you are looking at. 
2. Once you reach the leaf node, the node tells you the predicted outcome. 
3. All the edges are connected by ‘AND’.

**Feature Importance**
1. Go through all the splits for which the feature was used and measure how much it has reduced the variance or Gini index compared to the parent node. 
2. The sum of all importances is scaled to 100. 
3. This means that each importance can be interpreted as share of the overall model importance.

**When do we stop splitting?**
* Assign max depth 
* Assign a minimum difference of examples in a node 
* Go until the nodes are pure - this last one can introduce some overfitting

**How to deal with missing data?**
Surrogate splits. 

### Recommendations 

* This algorithm can be used to solve both classification and regression-based problems.
* It is particularly well suited to large datasets with high dimensionality as the algorithm inherently performs feature selection.
* The tree structure is ideal for capturing interactions between features in the data.
* The data ends up in distinct groups that are often easier to understand than points on a multi-dimensional hyperplane as in linear regression. *The interpretation is arguably pretty simple.*
* The tree structure also has a natural visualization, with its nodes and edges.
* There is no need to transform features. In linear models, it is sometimes necessary to take the logarithm of a feature. A decision tree works equally well with any monotonic transformation of a feature.
* *Trees fail to deal with linear relationships*. Any linear relationship between an input feature and the outcome has to be approximated by splits, creating a step function. This is not efficient.
* This goes hand in hand with *lack of smoothness*. Slight changes in the input feature can have a big impact on the predicted outcome, which is usually not desirable.
* Trees are also *quite unstable*. A few changes in the training dataset can create a completely different tree. This is because each split depends on the parent split. And if a different feature is selected as the first split feature, the entire tree structure changes. It does not create confidence in the model if the structure changes so easily.

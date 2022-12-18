# Decision Trees

## Glossary
* **Decision Trees**: a tree based model which traverses examples down to leaf nodes by the properties of the examples features. 
* * **CART - Classification and Regression Tree**: algorithm for constructing an approximate optimal decision tree for given examples. 
* **split point**: a pair of feature and feature value which is assigned to a node in a tree. This split point will determine which examples will go left and which examples will go right based on the feature and feature value. 
* **Gini impurity**: used as a way to determine the best split point for a given node in a classification tree. It is based on the probability of incorrectly classifying an item based on all of the items in the node. 
* **Surrogate split**: suboptimal split point reserved for examples which are missing the optimal split point feature. 
* **Boosting**: an ensemble technique which trains many weak learners sequentially , with each subsequent weak learner being trained on the previous weak learner's error. This generally reduces bias error. 
* **Bagging**: also bootstrap aggregation, a sampling technique which selects subsets of examples and/or features to train an ensemble of models. This generally reduces the variance error. 
* **Weak learner**: shallow decision trees. It generally can be an underfitting model. 

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

**When do we stop splitting?**
* assign max depth 
* assign a minimum difference of examples in a node 
* go until the nodes are pure - this last one can introduce some overfitting

**How to deal with missing data?**
Surrogate splits. 
### Recommended use
* This algorithm can be used to solve both classification and regression-based problems.
* It is particularly well suited to large datasets with high dimensionality as the algorithm inherently performs feature selection.

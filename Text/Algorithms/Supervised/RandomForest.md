## Random Forest

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

### Recommended use
* This algorithm can be used to solve both classification and regression-based problems.
* It is particularly well suited to large datasets with high dimensionality as the algorithm inherently performs feature selection.

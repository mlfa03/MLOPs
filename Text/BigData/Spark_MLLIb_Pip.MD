## Spark MLLIB Pipelines 

A Pipeline chains multiple Transformers and Estimators together to specify an ML workflow.

### Pipeline components 

#### Transformers 
*  Abstraction that includes feature transformers and learned models.
*  Implements a method transform(), which converts one DataFrame into another, generally by appending one or more columns. 

#### Estimators 
*  Abstracts the concept of a learning algorithm or any algorithm that fits or trains on data.
*  Implements a method fit(), which accepts a DataFrame and produces a Model, which is a Transformer.
*  For example, a learning algorithm such as LogisticRegression is an Estimator, and calling fit() trains a 
LogisticRegressionModel, which is a Model and hence a Transformer.




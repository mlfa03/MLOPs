## Naive Bayes

### Glossary 
* **Bernoulli Distribution** : A distribution which evaluates a particular outcome as binary. 
* **Laplace Smoothing** : A type of additive smoothing which mitigates the chance of encountering zero probabilities within the Naive Bayes classifier. 


### Main concepts 
* Naïve Bayes Classifier is one of the simple and most effective Classification algorithms which helps in building the fast machine learning models that can make quick predictions. 
* It is a probabilistic classifier, which means it predicts on the basis of the probability of an object.
* The Naive Bayes classifier calculates the class probabilities for each feature independently, which is equivalent to a strong (= naive) assumption of conditional independence of the features.

**Types**
* **Gaussian Naive Bayes classifier**: used when features are not discreet. 
* **Multinomial Naive Bayes Classifier**: used when features follow a multinomial distribution. 
* **Bernoulli Naive Bayes classifier**: used when features are of the boolean type.

### How does it work?

In machine learning we are often interested in selecting the best hypothesis (h) given data (d).In a classification problem, our hypothesis (h) may be the class to assign for a new data instance (d).Bayes’ Theorem provides a way that we can calculate the probability of a hypothesis given our prior knowledge.

Bayes’ Theorem is stated as:

*P(h|d) = (P(d|h) * P(h)) / P(d)*

Where

* **P(h|d)** is the probability of hypothesis h given the data d. This is called the posterior probability.
* **P(d|h)** is the probability of data d given that the hypothesis h was true.
* **P(h)** is the probability of hypothesis h being true (regardless of the data). This is called the prior probability of h.
* **P(d)** is the probability of the data (regardless of the hypothesis).

### Recommendations 
* **Categorical Inputs**: Naive Bayes assumes label attributes such as binary, categorical or nominal.
* **Gaussian Inputs**: the algorithm will perform better if the univariate distributions of your data are Gaussian or near-Gaussian. This may require removing outliers (e.g. values that are more than 3 or 4 standard deviations from the mean).
* **Classification Problems**: Naive Bayes is a classification algorithm suitable for binary and multiclass classification.
* **Log Probabilities**: The calculation of the likelihood of different class values involves multiplying a lot of small numbers together. This can lead to an underflow of numerical precision. As such it is good practice to use a log transform of the probabilities to avoid this underflow.
* **Kernel Functions**: Rather than assuming a Gaussian distribution for numerical input values, more complex distributions can be used such as a variety of kernel density functions.
Update Probabilities: When new data becomes available, you can simply update the probabilities of your model. This can be helpful if the data changes frequently.


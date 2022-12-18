## Causal Modelling in Machine Learning 

### Machine Learning and Causation - Some Issues

As you may know, ML algorithms in their current state can be biased, suffer from a relative lack of explainability, and are limited in their ability to generalize the patterns they find in a training data set for multiple applications. It has become important to improve generalization.

Current machine learning approaches tend to overfit the data. Indeed, they try to learn the past perfectly, instead of uncovering the real/causal relationships that will continue to hold over time.

Because Deep Learning (DL) has focused too much on correlation without causation, data won’t answer the question when the problem moves away from very narrow situations. Actually, a lot of real-world data is not generated in the same way as the data that we use to train AI models. In other words, Deep learning is good at finding patterns in terms of data, but can’t explain how they’re connected.

ML systems excel in learning connections between input data and output predictions, but lack in reasoning about cause-effect relations or environment changes. ML models that could capture causal relationships will be more generalizable.

### What is a causal model?

Causality: influence by which one event, process or state, a cause, contributes to the production of another event, process or state, an effect, where the cause is partly responsible for the effect, and the effect is partly dependent on the cause.

Addressing causality with traditional models lack two elements:
* Correlation has no directionality. When we know that A correlates with B we do not know which causes which. 
* There is no way to articulate what if scenarios 

**Experiments**

 Experiments must have the following characteristics: 
 * Controlled experiment
 * Sufficient sample size to address random guessing 
 * Careful design, including randomization 
 
 ### Skepticism 
 
 **About data**
 No accurate assessment of causal inference can take place if your data is biased. 
 
 
 **About results**
 Restriction of range 
 
 **About causes**
 "Correlation does not imply causation"
 
 
 ### Meta learning causal structures 
 In 2019, Yoshua Bengio and his team posted a research paper outlining an approach. Indeed they seem to be working on a version of deep learning capable of recognizing simple cause-and-effect relationships. They used a dataset that maps causal relationships between real-world phenomena, such as smoking and lung cancer, in terms of probabilities. They also generated synthetic datasets of causal relationships.

In other words “The resulting algorithm essentially forms a hypothesis about which variables are causally related, and then tests how changes to different variables fit the theory”. (4)

### SEM (Structural Equation Modelling)
the fundamental math established by Judea Pearl and the rapid evolution of graph models are helping make causality tools available” (5).

### Causal Bayesian Network 
This method estimates the relationships between all variables in a data set and can be considered as a true discovery method. It enables the discovery of multiple causal relationships at the same time.


### Reinforcement learning x Causality 
This type of learning is called “model-free” because it can learn effective behaviors without having to learn an explicit model of how the world works.

In reinforcement learning, a model-free algorithm is an algorithm that does not use the transition probability distribution (and the reward function) associated with the Markov decision process, which, in RL, represents the problem to be solved. 


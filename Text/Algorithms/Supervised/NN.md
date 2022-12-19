## Neural Networks

To make predictions with a neural network, the data input is passed through many layers of multiplication with the learned weights and through non-linear transformations. A single prediction can involve millions of mathematical operations depending on the architecture of the neural network.

### Glossary 

* **Gradient**: a vector of partial derivatives
* **Backpropagation**: The use of derivative chain rule along with dynamic programming to determine the gradients of the loss function in Neural Networks. 
* **Forward Pass**: calculating an output of a neural network for a particular input.
* **Momentum**: a concept applied to gradient descent in which the gradients applied to the weight updates depends on previous gradients. 
* **Adagrad**: an optimizer used to update the weights of a neural network in which different learning rates are applied to different weights. 
* **Adam**: a common gradient descent optimizer that takes advantage of momentum and adaptative learning rates. 
* **Vanishing gradient**: the repeated multiplication of large gradients resulting in an overflow or infinity-value products. 
* **Initialization techniques**: ways to initialize weights of a neural network in an attempt to avoiding vanishing and exploding gradients. 
* **Activation function**: the function used on the output of a neuron. These activations can be linear or non-linear. If they're non linear they can be symmetric or asymmetric. 
* **RELU**: Rectified Linear Unit is an asymetric activation function which outputs the value of the positive inputs and zero otherwise. 
* **Hyperbolic tangent**: a symmetric activation function which ranges from -1 to 1. 
* **L2 Loss** : the sum of squared errors of all the training examples. Not to be confused with L2 regularization. 
* **MAE**: the average of absolute differences across training examples. 
* **Dropout**: a regularization technique used per layer to reduce overfitting. It involves randomly omitting neurons from the neural network structure at each training iteration. Effectively, dropout produces an ensemble of neural networks. Dropout is incomplete without adjusting for the dropout in preparation for prediction. 
* **Pruning neurons**: removing neurons from a neural network in an effort to reduce the number of model parameters. 

### Main concepts 


### How does it work?


### Recommended use

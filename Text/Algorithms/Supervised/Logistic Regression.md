## Logistic Regression



* Classification algorithm that assigns observations to discrete set of classes.  

* Predictions fall into a range starting from 0 to 1.

* Does not require a linear relationship between predictions and predictors

#### How does it work?

* Sigmoid function to predict output.

![image](https://user-images.githubusercontent.com/39881974/200902384-7952c15d-74e7-44d6-bffb-4a39a04f8784.png)


* X is a matrix containing input features and theta is the randomly initialized values that will be updated in the algorithm. 

![image](https://user-images.githubusercontent.com/39881974/200902342-18b4aacd-0a78-4651-ac8b-63573de2c112.png)

 
* A cost function gives the measure of how far the predicted output is from the original labels (‘y’ vector). ‘m’ is the number of training data. 

![image](https://user-images.githubusercontent.com/39881974/200902235-6df9690c-85dc-447e-ae44-44075edbb7bf.png)

* Theta values are updated to minimize the cost function. 

![image](https://user-images.githubusercontent.com/39881974/200902301-d9499aa2-2ed5-4a31-8136-5bac56d759f4.png)

# Machine Learning Technical Debt 

Source: https://proceedings.neurips.cc/paper/2015/file/86df7dcfd896fcaf2674f757a2463eba-Paper.pdf

ML systems have a special capacity for incurring technical debt, because they have all of the maintenance problems of traditional code plus an additional set of ML-specific issues. This debt may be difficult to detect because it exists at the system level rather than the code
level.

## Complex Models Erode Boundaries

### Entanglement 
* Machine learning systems mix signals together, entangling them and making isolation of improvements impossible.
* No inputs are ever really independent. We refer to this here as the CACE principle: Changing Anything Changes Everything.
* CACE applies not only to input signals, but also to hyper-parameters, learning settings, sampling methods, convergence thresholds,
data selection, and essentially every other possible tweak.

### Correction Cascades
The cost increases when correction models are cascaded, with a model for problem A′′ learned on top of m′a, and so on,
for several slightly different test distributions. Once in place, a correction cascade can create an improvement deadlock, as improving the accuracy of any individual component actually leads to system-level detriments.

### Undeclared Consumers
* Oftentimes, a prediction from a machine learning model ma is made widely accessible, either at runtime or by writing to files or logs that may later be consumed by other systems. 
* Without access controls, some of these consumers may be undeclared, silently using the output of a given model as an input to another system. 
* In more classical software engineering, these issues are referred to as visibility debt.

## Data Dependencies Cost More than Code Dependencies 

### Unstable data dependencies 


### Underutilized data dependencies 


### Static analysis of data dependencies 


## Feedback loops 

### Direct Feedback Loops 

### Hidden Feedback Loops 


## ML Systems Anti-Patterns 

### Glue Code 


### Pipeline Jungles 


### Dead Experimental Codepath 


### Abstraction debt 


### Common smells 


## Other ML Related debt 

### Data testing debt 


### Reproducibility debt 

### Process management debt 


### Cultural debt 

## Configuration debt 


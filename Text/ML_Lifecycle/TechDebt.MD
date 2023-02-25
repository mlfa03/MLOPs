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
Some input signals are unstable, meaning that they qualitatively or quantitatively change behavior over time. This can happen implicitly,
when the input signal comes from another machine learning model itself that updates over time, or a data-dependent lookup table, such as for computing TF/IDF scores or semantic mappings. It can also happen explicitly, when the engineering ownership of the input signal is separate from the engineering ownership of the model that consumes it.

### Underutilized data dependencies 
Underutilized dependencies are packages that are mostly unneeded. Similarly, underutilized data dependencies are input signals that provide little incremental modeling benefit. These can make an ML system unnecessarily vulnerable to change, sometimes catastrophically so, even though they could be removed with no detriment.

### Static analysis of data dependencies 


## Feedback loops 

### Direct Feedback Loops 
A model may directly influence the selection of its own future training data. It is common practice to use standard supervised algorithms, although the theoretically correct solution would be to use bandit algorithms. 

### Hidden Feedback Loops 
Direct feedback loops are costly to analyze, but at least they pose a statistical challenge that ML researchers may find natural to investigate. A more difficult case is hidden feedback loops, in which two systems influence each other indirectly through the world. 

## ML Systems Anti-Patterns 

### Glue Code 
ML researchers tend to develop general purpose solutions as self-contained packages. 

### Pipeline Jungles 
As a special case of glue code, pipeline jungles often appear in data preparation. These can evolve organically, as new signals are identified and new information sources added incrementally. Without care, the resulting system for preparing data in an ML-friendly format may become a jungle of scrapes, joins, and sampling steps, often with intermediate files output. Managing these pipelines, detecting errors and recovering from failures are all difficult and costly.

### Dead Experimental Codepath 


### Abstraction debt 


### Common smells 


## Other ML Related debt 

### Data testing debt 


### Reproducibility debt 

### Process management debt 


### Cultural debt 

## Configuration debt 


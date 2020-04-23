## Section 4: Weight Initialization

### Why not 0, random numbers
The updates to the weights is dependent on the previous weights. We will never be able to update these weights and no learning will occur.  
Gradients might vanish and explode with just random thrown numbers.

### Normal Distribution  
One solution.
- Initialize the weights from a specific range.
- Take them from a normal distribution with a mean of zero and a standard devicaiton of 1. 

### When all weights are initialized to the same value  
All weights will get updated with the same value and they will be equal.  
**Symmetry Breaking Problem**  

### Xavier Initialization (Sigmoid activation, linear)
[Understanding the diffulty of training deep feedforward neural networks 2009](http://proceedings.mlr.press/v9/glorot10a/glorot10a.pdf)  
We want the weights to remain in a specific range, so we expect the to have the same variance as the inputs.  

### He Norm Initialization (ReLU activation, nonlinear)
[Delving deep into rectifiers: surpassing human-level performance on imageNet classification(2015)](https://arxiv.org/pdf/1502.01852.pdf)  
Var(W) = 2/n_in  









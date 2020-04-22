## Section 4: Weight Initialization

## Why not 0, random numbers
The updates to the weights is dependent on the previous weights. We will never be able to update these weights and no learning will occur.  
Gradients might vanish and explode with just random thrown numbers.

## Normal Distribution  
One solution.
- Initialize the weights from a specific range.
- Take them from a normal distribution with a mean of zero and a standard devicaiton of 1. 








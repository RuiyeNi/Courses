## Section 2 Loss Functions
**Objective**: minimize the loss between the predictions and actual outputs.

### Mean Squared Error (MSE)
```python
MSE = 1/n*Sum(Y_i -Y^i)^2  
```
- Y^i predicted output 
- Y_i actual output 
- n minibatch smaples or all training samples  

Variations:
- Half of the MSE: 1/(2n)*Sum(Y_i - Y^i)^2  
- Root MSE (RMSE): MSE^(1/2). 

Note on the side:  
If there is more than one output neuron, need to add the error for each output neuron, in each of the training samples.  
MSE = sum(1/n*Sum(Y_i-Y^i)^2)  

### L2 Loss (MSE)
Convex, only one minimum. MSE is high for large loss values and decreases as loss approaches 0. 

### L1 Loss Mean Absolute Error (MAE)
```python
MAE = 1/n*sum(|Y_i - Y^i|)  
```

L2 vs L1:  
- L2 is more sensitive to outliers than L1. When there is large deviations, the error is big. L2 will try to adjust the model according to the outliers values, even at the expense of other samples.  
- L1 is more robust and is generally not affected by outliers.  

### Huber Loss (Smooth L1 Loss). 
Combine L2 and L1.
How small the error has to be to make it quadratic depends on a hyperparameter: delta, which can be tuned. 
```python
if |y - f(x)| <= delta:
    L(y, f(x)) = 1/2*(y-f(x))^2
else:
    L(y, f(x)) = delta*|y-f(x)| - 1/2*delta^2 
```
### Binary Cross Entropy Loss  (BCE)
- used when the output lables have values of 0 or 1
- can also be used when the output labels have values between 0 and 1
```python
L = -1/n Sum_samples Sum_classes[ylog(p) + (1-y)log(1-p)]
```
- each sample takes either ylog(p) or (1-y)log(1-p)
- sum_classes is needed for multi-label classification, e.g. an image has multiple objects  



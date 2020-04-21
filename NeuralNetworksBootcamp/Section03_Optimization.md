## Section03 Optimization  
### Gradient Descent
The base algorithm that is used to minize the error with respect to the weights of the neural network. An Epoch is one compelte 
pass through all the samples. 
- **Batch Gradient Descent**  
  + All the sampels are passed to the neural network at one time.
  + iteration = epoch
- **Stochastic Gradient Descent**  
  + takes in one sample at each iteration, perform the weight update for each sample a time
  + iteration per epoch = number of samples
  + high variance of updates and causes teh function to fluctuate
- **Mini-Batch Gradient Descent**  
  + takes the best of both the batch and stochastic gradient descent
  + perform weight update for a batch of samples
  + take n training samples/per batch to update model

### Exponentially Weighted Average
V_t = beta*V_t-1 + (1 - beta) & theta_t
- beta = 0.9, average over 1/(1-0.9)= 2 points
- bias correction of exponentially weighted average, divide d_t by (1-beta^t)

### Momentum
Use exponentially moving average to reduce the oscillations in the vertical direction and speed it up in the horizontal direction!  
Accelerates the SGD in the correct direction and weakens the oscillations, by adding a fraction gamma for the past update vector the new update vector. 

### RMSProp
RMSProp is an adaptive learning rate method.  
- Proposed by Geoff Hinton in his Coursera Class
- RMSProp divides the learning rate by an exponentially decaying average of squared grdinets
- Gamma is suggested to be 0.9 and learning rate = 0.001
- Horizontal direction gets larger learning rate to increase the speed
- Vertical direction gets smaller learning rate to decrease the speed

### Adam Optimization (Adaptive Moment Estimation) 
- Learnigng rate is adaptive
- Stores an exponentially decaying average of past square gradients (Vt)
- Stores an exponentially decaying average of past gradients (mt)

### SWATS - Switching from Adam to SGD
Start training deep neural network with Adam but then swtich to SGD when certain criteria hits to obtain better generalization power. Adam in some areas does not converge to an optimal solution.

### Weight Decay and Regularization
Adding L2 regularization term to the cost function.  
E~(W) = E(W) + lambda/2*W^2  
w <- w - theta(delta(E)/delta(W)) - theta*lambda*W  
Subtract a little portion of the weight at each step, hence the name decay. 

Decay vs Regularization:
- Adding the L2 regularization term to the loss function -> L2 regularization  
- Only modify the weight update rule directly -> Weight decay
- These two are the same for **vanilla SGD**
- These two are not the same when adding Momentum or using Adam, L2 regularization != Wegiht decay 

### Decoupling Weight Decay  
<object data="http://yoursite.com/the.pdf" type="application/pdf" width="700px" height="700px">
<embed src="http://yoursite.com/the.pdf">
<p>This browser does not support PDFs. Please download the PDF to view it: Download PDF.</p>
</embed>
</object>




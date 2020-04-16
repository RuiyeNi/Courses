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

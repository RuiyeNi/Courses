## Section 5: Regualization and Normalization  

### Overfitting  
Get a high accuracy on the training data, but a low acccuracy on the test data.

### Reduce Overfitting  
Without any regularization:
- Train on more data
- Use data augmentation
- Use early stopping:
  + When validation error starts increating
  + or validation error not improving  

### Regularization Techniques
**L1/L2 Regularization:**
- Generate smaller weights  

**Dropout:** 
In the training phase, for each specific hidden layer, for each training sample, for each iteration, randomly disable a fraction, p, of neurons (and corresponding activations).  
Training time for each epoch is less, but roughly doubles the number of iterations required to converge. 

**Normalization:**  [0, 1]
Min-Max Normalization
x_scale = (x - x_min)/(X_max - X_min)  

**Standardization**  
x = (x-mean)/std

**Batch Normalization**  
Normalize each feature (each neuron) in a layer according to **the batch of samples**. The mean and standard deviation are calculated across a batch of samples.   
[Batch Normalization](https://arxiv.org/abs/1502.03167)    
Benifits of Batch Normalization      
- Converges fater and reduced the need for dropout.  
- Allowed the network to normalize a layer into whichever distribution is most optimal for learning, standardization is a special case of normalization. The parameters used for normalization are learnable.   
- Eliminates the need for a bias for a layer when batch normalization is applied to it.  

**Layer Normalization**  
Normalize each feature (each neuron) in a layer according to **the features in that layer**. The mean and standard deviation are calculated across the features of a layer.   

**Batch Normalization vs Layer Normalization**      
- All the normalization is calculated using: x = (x-mean)/std      
- Batch normalization and layer normalization are performed in different directions (it only differs in how - the mean is calculated)  
- For batch normalization, different samples for the same features in one mini batch are normalized. For layer normalization, different features from the sample are normalized without consideration of mini batch.  





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
[B](https://arxiv.org/abs/1502.03167)




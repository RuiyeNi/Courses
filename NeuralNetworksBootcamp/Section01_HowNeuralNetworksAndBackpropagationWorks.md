## Section1: How Neural Networks and Backpropagation works

### 1. What Can Deep Learning Do?
- Object detection
- Generate faces, GANs  
  + Cycle GANs  
  + Insta GANs  
  + Text-to Image Synthesis  
  + Super-Resolution (2016)
- Image Captioning  
- Dense Captioning  
- Scene Graph Generation  
- Visual Question Answering  
- Semantic Segmentation  
- Instance Segmentation  
- Image Colorization  
- Machine Translation seq2seq  
- Music Generation 

### 2. The Rise of Deep Learning
#### Timeline
 - Neural network 19's  
 - LSTM 1997  
 - CNN 1998  
 - Deep Learning 2012  

#### Three reasons
 - Availability of Datasets: 1M Images  
 - Availability of Computational Resources: GPUs  
 - Ability of deploy matrix multiplication to perform on GPUs: Nivida CUDA
    - forward/backword convolution
    - pooling
    - normalization 
    - activation layers  
  - Trigger: ImageNet Classification with Deep Convolutional Neural Networks Geoffrey E. Hinton
  
 ### 3. The Essence of Neural Networks
 Integrate inputs with corresponding weights with further linear/nonlinear activation, and yield a prediciton value.  
 
 ### 4. The Perceptron 
 Brain analogy: 2.5 PB can hold 3M hours of TV shows,run 300 years.   
 Percpetron, a single layer architecture, is a linear classifier which works for linearly seperable problem.  
 For XOR problem which is nonliear, multilayer perceptron (MLP) is neeed.   
 
 ### 5. Activation Functions in Deep Learning  
 #### Why do we need activations?
 Real world data cannot be sepearted linearly with a line. Activations functions represent non-linear complex arbitrrary functional mappings between inputs and outputs.  
 
 ### 6. Famous Types of Activation Functions
 - Sigmoid Activation (gating operations)
   + scale to a value [0, 1]
   + Disadvantage:
    * gradient vanish when input is small
    * explode when input is big
    * optimization gets harder because output is not 0 centered (0.5).
   + Derivative: y(1-y)
 - Hyperbolic Tan Activation (RNN)
   + scale to a value [-1, 1] 
   + Disadvantage: gradient vanish
   + Advantage: 0 centered, optimization is easier 
 - ReLU (Rectified Linear Unit) (CNN and hidden layers)
   + negative -> 0, positie -> no change
   + Disadvantage: if graients die (turns to 0), ReLU never activate on any input
 - Leaky ReLU (When ReLU suffers from dead neurons)
   + alpha to replace 0 in ReLU
   
### 7. Gradient Descent  
The Backpropagation
- Objective: minimize the error by changing the weight   
- Negative slope: increase w, the loss function is decreasing  
- Positive slope: increase w, the loss function is increasing  

Weight Update Rule  
- learning rate: how fast we update the weight, the step size of the udpate  
- new_weight = old_weight  - learning_rate * gradient
  
### 8. The Forward Propagation  
input -> weight -> activation -> output

### 9. Backpropagation
The Chain Rule  
- First term: How much is the error changing with respect to the output?
- Second term: How much is the output changing with respect to the input?
- Third term: How much is the input changing with respect to the weight?  



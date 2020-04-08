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
 

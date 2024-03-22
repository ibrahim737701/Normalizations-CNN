# TSAIAssignment8

# Normalization in Neural Networks Assignment

## Introduction

This assignment involves the implementation and understanding of a Convolutional Neural Network (CNN) using PyTorch, The given code defines a CNN architecture that can be used for image classification tasks. The model, named `Net`, includes several convolutional layers, batch normalization layers, max pooling layers, and an adaptive average pooling layer leading to a final convolutional layer for classification.



1. **Convolutional Layers**: The model includes several convolutional layers (`conv1` to `conv11`). These layers are responsible for extracting features from the input images. The first convolutional layer (`conv1`) takes an input with 3 channels (RGB image) and produces 16 feature maps. The subsequent layers further refine these features by applying more convolutions.

2. **Batch Normalization Layers**: Following each convolutional layer, batch normalization (`bn1` to `bn10`) is applied. Batch normalization helps in stabilizing the learning process and reducing the training time by normalizing the input to each activation layer.

3. **Max Pooling Layers**: The model utilizes max pooling (`pool1` and `pool2`) to reduce the spatial dimensions of the feature maps, thus reducing the computational load and overfitting.

4. **Adaptive Average Pooling Layer**: The global average pooling (`gap`) layer reduces each feature map to a single value, preparing the feature representation for classification.

5. **Classification Convolutional Layer**: The final convolutional layer (`conv11`) reduces the number of output channels to the number of classes in the dataset (e.g., 10 for CIFAR-10).

6. **Activation Functions**: The model uses the ReLU activation function after each batch normalization layer to introduce non-linearity, allowing the network to learn complex patterns.

   # Learnings

**Concept**: 

**Batch Normalization** normalizes the input of a layer for each mini-batch. It computes the mean and variance for the inputs of the mini-batch, then normalizes them. This helps in reducing the internal covariate shift which in turn stabilizes and speeds up the network's training. It also allows for higher learning rates and reduces the sensitivity to initialization.

**Group Normalization** divides the channels into groups and computes the mean and variance for normalization within each group. Unlike Batch Normalization, GN's operation is independent of batch sizes, making it suitable for tasks with small batch sizes or varying batch sizes during training.

**Layer Normalization** normalizes the inputs across the features instead of the batch dimension. It computes the mean and variance used for normalization from all of the summed inputs to the neurons in a layer on a single training case.


**Practical**


LayerNorm doesn't work well with image data.


<img width="1313" alt="Screenshot 2024-03-23 at 1 54 10 AM" src="https://github.com/ibrahim737701/TSAIAssignment8/assets/51760306/132a87e0-3b3c-4bd6-bacb-1e06fd1ae22b">

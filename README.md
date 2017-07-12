# Traffic-Sign-Classification

# Objective
Design, train and test a neural network model architecture for German Traffic Signs classification

# Data set Summary
Size of Training Set:   34799 samples
Size of Validation Set: 4410 samples
Size of Test Set:       12630 samples
Shape of a sample: (32,32,3)
Number of unique classes: 43

#Pre-processing the data
Step 1: Added additional training samples by adding noise to the existing images.

Step 2: Converted all the training samples to grayscale because the result is not dependent on the color channels.

Step 3: Normalized the data with the formula (image_data-128)/128. This is done so as to avoid impact of images with big weights.

# Network architecture

## The Layers in the network are as below:
# Layer 1:
    Type: Convolutional. 
    Input = 32x32x1. Output = 28x28x6.
    Pooling: Input = 28x28x6. Output = 14x14x6.

# Layer 2:
    Type: Convolutional
    Input =14x14x6 Output = 10x10x16
    Pooling : Input = 10x10x16. Output = 5x5x16

# Layer 3:
    Type: Convolutional
    Input = 5x5x16. Output = 1x1x32

# Layer 4:
    Type:Fully connected
    Input = 32. Output = 120

# Layer 5:
    Type:Fully connected
    Input = 120. Output = 84

# Layer 6:
    Type:Fully connected
    Input = 84. Output = 32

# Layer 7:
    Type:Fully connected
    Input = 32. Output = 43

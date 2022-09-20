# Traffic-Sign-Classification-Using-Le-Net

## Introduction
***
Traffic sign classification is an important task for self driving cars.
In this project, a Deep Network known as LeNet will be used for traffic sign images classification.

## Table of Contents
***
1. [About Data](#About-Data)
2. [Overview](#Overview)
3. [Le-Net Architecture](#Le-Net-Architecture)
4. [Model Evaluation](#Model-Evaluation)


## About Data
***
* The dataset contains 43 different classes of images.
* Format: Image Data
* Images are 32 x 32 pixels

## Overview
***
<img width="650" alt="image" src="https://user-images.githubusercontent.com/71331819/191171263-2860812a-bf2f-4ba6-92df-2f6650d57e5f.png">

## Le-Net Architecture
***
<img width="650" alt="image" src="https://user-images.githubusercontent.com/71331819/191171419-a9bea130-4bcc-4602-8407-0263d6afbb2b.png">

### STEP 1: THE FIRST CONVOLUTIONAL LAYER
```
Input = 32x32x1  
Output = 28x28x6  
Output = (Input-filter+1)/Stride* => (32-5+1)/1=28  
Used a 5x5 Filter with input depth of 3 and output depth of 6  
Apply a RELU Activation function to the output  
pooling for input, Input = 28x28x6 and Output = 14x14x6  
```

### STEP 2: THE SECOND CONVOLUTIONAL LAYER
```
Input = 14x14x6 
Output = 10x10x16 
Layer 2: Convolutional layer with Output = 10x10x16 
Output = (Input-filter+1)/strides => 10 = 14-5+1/1 
Apply a RELU Activation function to the output 
Pooling with Input = 10x10x16 and Output = 5x5x16 
```

### STEP 3: FLATTENING THE NETWORK
```
Flatten the network with Input = 5x5x16 and Output
```

### STEP 4: FULLY CONNECTED LAYER
```
Layer 3: Fully Connected layer with Input = 400 and Output = 120 
Apply a RELU Activation function to the output 
```

### STEP 5: SECOND FULLY CONNECTED LAYER
```
Layer 4: Fully Connected Layer with Input = 120 and Output = 84 
Apply a RELU Activation function to the output 
```

### STEP 6: FULLY CONNECTED LAYER
```
Layer 5: Fully Connected layer with Input = 84 and Output = 43
```

## Model Evaluation
***
* Trained the model for 50 epochs.
* Loss function: sparse_categorical_crossentropy
* Batch size: 500

Test Accuracy : 0.8572

The following graphs show the relationship between loss and accuracy of training and validation dataset.
<img width="400" alt="image" src="https://user-images.githubusercontent.com/71331819/191173166-91d445ce-75ff-4969-901c-3eb8f65c96ff.png">
<img width="400" alt="image" src="https://user-images.githubusercontent.com/71331819/191173204-0ae09531-786f-47c0-8278-76c8a116ab55.png">


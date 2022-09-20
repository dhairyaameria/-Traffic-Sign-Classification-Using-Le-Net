# Traffic-Sign-Classification-Using-Le-Net

## Introduction

Traffic sign classification is an important task for self driving cars.
In this project, a Deep Network known as LeNet will be used for traffic sign images classification.

## Table of Contents
1. [About Data](#About Data)
2. [Overview](#Overview)
3. [Le-Net Architecture](#Le-Net Architecture)
4. [Collaboration](#collaboration)
5. [FAQs](#faqs)

## About Data
The dataset contains 43 different classes of images.
Format: Image Data
Images are 32 x 32 pixels

## Overview
<img width="650" alt="image" src="https://user-images.githubusercontent.com/71331819/191171263-2860812a-bf2f-4ba6-92df-2f6650d57e5f.png">

## Le-Net Architecture
![image](https://user-images.githubusercontent.com/71331819/191171419-a9bea130-4bcc-4602-8407-0263d6afbb2b.png)

### STEP 1: THE FIRST CONVOLUTIONAL LAYER #1
'''
Input = 32x32x1  
Output = 28x28x6  
Output = (Input-filter+1)/Stride* => (32-5+1)/1=28  
Used a 5x5 Filter with input depth of 3 and output depth of 6  
Apply a RELU Activation function to the output  
pooling for input, Input = 28x28x6 and Output = 14x14x6  
'''


# Improved CNN Model for CIFAR-10 Classification in MATLAB

## Overview

This project implements a **Convolutional Neural Network (CNN)** in **MATLAB** to classify images from the **CIFAR-10 dataset**. The model is trained using an improved CNN architecture with batch normalization, dropout, and data augmentation to enhance performance.

## Dataset

The CIFAR-10 dataset consists of **60,000 32×32 color images** in **10 classes**, with **6,000 images per class**. The dataset is divided into:

-   **50,000 training images**
-   **10,000 test images**

### Classes:

1.  Airplane
2.  Automobile
3.  Bird
4.  Cat
5.  Deer
6.  Dog
7.  Frog
8.  Horse
9.  Ship
10.  Truck

## Features of the Model

-   Uses **Convolutional Layers** to extract features from images.
-   **Batch Normalization** for stable training.
-   **Dropout Layers** to prevent overfitting.
-   **Data Augmentation** to improve model robustness.
-   Trained with the **Adam optimizer** and a **learning rate scheduler**.

## Prerequisites

Ensure that you have MATLAB installed with the following toolboxes:

-   **Deep Learning Toolbox**
-   **Image Processing Toolbox**
-   **Statistics and Machine Learning Toolbox** (optional)

## Installation

1.  Clone the repository:
    
    ```bash
    git clone https:https://github.com/NazrulFaran/cnn-cifar10-matlab.git
    
    ```
    
2.  Download the CIFAR-10 dataset (MATLAB format) and place it in the project folder.

## Running the Model

1.  Open MATLAB and navigate to the project folder.
2.  Run the script:
    
    ```matlab
    cnn_cifar10_matlab
    
    ```
    
3.  The model will be trained and tested, displaying the training progress and test accuracy.

## Expected Output

-   **Training Accuracy:**  **81.21%**
    
-   **Test Accuracy:**  **80.59%**
    
-   **Sample Image Predictions:** The model will display 20 randomly selected test images along with their predicted labels.

## Results Visualization

-   Training accuracy and loss curves will be displayed during training.
-   A subplot of test image predictions will be shown after evaluation.

## Model Architecture

```matlab
layers = [
    imageInputLayer([32 32 3])
    convolution2dLayer(3, 32, 'Padding', 'same')
    batchNormalizationLayer
    reluLayer
    ...
    fullyConnectedLayer(10)
    softmaxLayer
    classificationLayer
];

```

## File Structure

```
📂 cnn-cifar10-matlab/
├── 📄 cnn_cifar10_matlab.mlx   # Main MATLAB script
├── 📂 cifar-10-batches-mat/  # CIFAR-10 dataset folder
├── 📄 README.md              # Project documentation

```

## Author

**Nazrul Islam**

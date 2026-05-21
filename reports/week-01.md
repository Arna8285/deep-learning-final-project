# Project Title  
Image Classification using Convolutional Neural Networks (CNNs) and MLP on Real-World Scene Images  


# Problem Statement  

## What problem are you trying to solve?  
The goal of this project is to develop deep learning models that can automatically classify images of natural and urban scenes into predefined categories such as:  
buildings, forest, mountains, sea, glacier, and street.


## Why is this problem useful or interesting?  
Image classification is a key task in computer vision with many real-world applications, including:  
- surveillance systems  
- autonomous vehicles  
- environmental monitoring  
- smart city technologies  

Automating image recognition helps process large-scale visual data efficiently and accurately.


## What will the model predict or generate?  
The model takes an image as input and predicts its corresponding class label (e.g., forest, sea, street).


# Dataset  

## Dataset Name  
Intel Image Classification Dataset (Kaggle)  
https://www.kaggle.com/datasets/puneet6060/intel-image-classification  

## Why this dataset?  
- Real-world scene images  
- More complex than basic datasets like CIFAR-10  
- Suitable for CNN-based image classification  

# Models Used  

## 1. Convolutional Neural Network (CNN)  
A deep learning model designed for image feature extraction.

### Architecture:
- Convolutional layers  
- Max Pooling layers  
- Fully connected layers  
- Dropout  
- Batch Normalization  

## 2. Multilayer Perceptron (MLP) – Baseline Model  
A fully connected neural network used as a baseline for comparison.

### Architecture:
- Flattened image input  
- Dense layers  
- ReLU / Softmax activation  
- No spatial feature extraction  

# Batch Normalization  
Batch Normalization was added to the CNN model to:
- stabilize training  
- speed up convergence  
- reduce internal covariate shift  
- improve overall performance  

# Loss Function  
Cross-Entropy Loss  

# Evaluation Metrics  
- Accuracy  
- Precision  
- Recall  
- F1-score  

# Train/Validation/Test Split  
- 80% Training  
- 10% Validation  
- 10% Testing  

# Experiments and Comparison  

## CNN vs MLP  

| Model | Strengths | Weaknesses |
|------|----------|------------|
| CNN | Strong feature extraction, high accuracy, good generalization | Higher computational cost |
| MLP | Simple baseline, fast training | Poor performance on image data |

## Key Insight  
CNN significantly outperforms MLP because it learns spatial features from images, while MLP treats images as flat vectors.

Batch Normalization improves CNN training stability and performance.

# Expected Challenges  
- Overfitting  
- Limited computational resources  
- Hyperparameter tuning  
- Possible class imbalance  

# Proposed Improvements  
- Data augmentation:
  - flipping  
  - rotation  
  - zooming  

- Regularization:
  - Dropout  
  - Batch Normalization  

- CNN architecture tuning  


# Expected Results  
- CNN accuracy: ~70–85%  
- MLP accuracy: lower baseline performance  
- Improved stability with Batch Normalization  
- Clear performance gap between CNN and MLP  


# Conclusion  
This project demonstrates the effectiveness of CNNs compared to MLPs for image classification tasks.  

It also shows that Batch Normalization improves training stability and model performance. Overall, CNNs are significantly better suited for real-world image recognition problems due to their ability to learn spatial features.

# Project Title  
Image Classification using Convolutional Neural Networks (CNNs) and MLP on Real-World Scene Images  

# 1. Problem Statement  

The goal of this project is to develop deep learning models capable of automatically classifying real-world scene images into predefined categories:

- buildings  
- forest  
- mountains  
- sea  
- glacier  
- street  

This is a multi-class image classification problem using deep learning.

# 2. Dataset Description  

The dataset used is the **Intel Image Classification Dataset (Kaggle)**:  
https://www.kaggle.com/datasets/puneet6060/intel-image-classification/data  

It contains approximately **25,000 images** of real-world scenes.

### Classes:
- Buildings  
- Forest  
- Glacier  
- Mountain  
- Sea  
- Street  

### Dataset Split:
- Training set: ~14,000 images  
- Test set: ~3,000 images  
- Prediction set: ~7,000 images (unlabeled)  

All images are resized to **150 × 150 pixels**.

# 3. Data Preprocessing  

The following preprocessing steps were applied:

- Image resizing to 150 × 150  
- Normalization (pixel values scaled to [0, 1])  
- Label encoding for categorical classes  
- Data augmentation:
  - horizontal flipping  
  - rotation  
  - zooming  

These steps improved generalization and reduced overfitting.

# 4. Model Architecture  

## 4.1 CNN Model  

A Convolutional Neural Network was built with the following architecture:

- Convolutional layers (feature extraction)  
- MaxPooling layers (dimensionality reduction)  
- Batch Normalization (stabilizing training)  
- Dropout (regularization)  
- Fully connected dense layers  
- Softmax output layer (6 classes)  

## 4.2 MLP Model (Baseline)  

A Multilayer Perceptron was used as a baseline:

- Flatten input layer  
- Fully connected dense layers  
- ReLU activation  
- Softmax output layer  

MLP does not preserve spatial information in images.

# 5. Training Setup  

- Loss function: Cross-Entropy Loss  
- Optimizer: Adam  
- Batch size: 32 (adjusted during experiments)  
- Epochs: 10–30 (depending on model)  
- Train/Validation split: 80% / 10% / 10%  

# 6. Evaluation Metrics  

The following metrics were used:

- Accuracy  
- Precision  
- Recall  
- F1-score  
- Confusion Matrix (for error analysis)

# 7. Results  

## 7.1 Model Comparison  

| Model | Accuracy | Precision | Recall | F1-score | Notes |
|------|----------|-----------|--------|----------|------|
| CNN | ~75–85% | High | High | High | Best performance |
| MLP | ~50–65% | Medium | Low | Low | Baseline model |

## 7.2 Key Observations  

- CNN significantly outperformed MLP in all metrics  
- Batch Normalization improved training stability  
- Data augmentation reduced overfitting  
- MLP struggled with spatial feature extraction  

# 8. Error Analysis  

Common mistakes made by the CNN model:

- Confusion between **mountain and glacier**  
- Misclassification of **sea vs street in low-quality images**  
- Errors in images with poor lighting or ambiguous scenes  

These errors are due to visual similarity between classes.

# 9. Limitations  

- Limited computational resources  
- No use of pre-trained models (e.g., ResNet)  
- Model trained from scratch only  
- Some class overlap in dataset  
- Fixed image size (loss of detail)

# 10. Conclusion  

This project demonstrates that Convolutional Neural Networks are highly effective for real-world image classification tasks.

Key conclusions:

- CNN significantly outperforms MLP  
- Spatial feature learning is crucial for image tasks  
- Batch Normalization improves training stability  
- Data augmentation enhances generalization  

Overall, CNN is the most suitable model for this dataset.

# 11. References  

- Intel Image Classification Dataset (Kaggle):  
https://www.kaggle.com/datasets/puneet6060/intel-image-classification  

- TensorFlow Documentation:  
https://www.tensorflow.org/  

- Keras Documentation:  
https://keras.io/  

- Deep Learning Book (Goodfellow et al.)  

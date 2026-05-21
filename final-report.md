# Project Title  
Image Classification using Convolutional Neural Networks (CNNs) and Multilayer Perceptron (MLP) on Real-World Scene Images  

# 1. Problem Statement  

Image classification is a fundamental problem in computer vision where the goal is to assign a label to an input image.

In this project, the objective is to build and compare two deep learning models:

- Convolutional Neural Network (CNN)  
- Multilayer Perceptron (MLP) as a baseline  

The models are trained to classify real-world scene images into six categories:

- buildings  
- forest  
- mountains  
- sea  
- glacier  
- street  

The main goal is to analyze how architecture choice affects performance on real image data.

# 2. Dataset Description  

The dataset used is the **Intel Image Classification Dataset (Kaggle)**:  
https://www.kaggle.com/datasets/puneet6060/intel-image-classification/data  

It contains approximately **25,000 labeled images** of natural and urban scenes.

## Classes:
- Buildings  
- Forest  
- Glacier  
- Mountain  
- Sea  
- Street  

## Dataset Split:
- Training set: ~14,000 images  
- Test set: ~3,000 images  
- Prediction set: ~7,000 images (unlabeled)  

All images are resized to **150 × 150 × 3 (RGB)**.

## Dataset Characteristics:
- Real-world variability (lighting, angle, background complexity)  
- Balanced multi-class distribution  
- High intra-class similarity (e.g., mountain vs glacier)  
- Suitable for deep CNN evaluation  

# 3. Data Preprocessing  

To prepare the dataset for training, the following preprocessing steps were applied:

## 3.1 Image Processing
- Resizing all images to 150×150 pixels  
- Converting images to normalized float values (0–1 scaling)  
- One-hot encoding of labels  

## 3.2 Data Augmentation (CNN only)
To improve generalization and reduce overfitting:

- Random horizontal flipping  
- Random rotation  
- Zoom augmentation  
- Slight shifts and transformations  

## 3.3 Why preprocessing matters
These steps help the model:
- reduce overfitting  
- generalize better on unseen images  
- handle real-world variations  

# 4. Model Architecture  

## 4.1 CNN Model (Main Model)

The CNN architecture consists of:

- Conv2D layers (feature extraction)  
- MaxPooling layers (downsampling)  
- Batch Normalization layers  
- Dropout layers (regularization)  
- Fully connected Dense layers  
- Softmax output layer (6 classes)  

### Key idea:
CNN learns spatial hierarchies:
- edges → textures → shapes → objects  

## 4.2 MLP Model (Baseline)

The MLP model is a fully connected neural network:

- Flatten layer (image → vector)  
- Dense hidden layers  
- ReLU activation  
- Softmax output layer  

### Limitation:
MLP does NOT preserve spatial structure of images.

## 4.3 Batch Normalization  

Batch Normalization was added to CNN to:

- stabilize gradients  
- reduce internal covariate shift  
- speed up convergence  
- allow higher learning rates  

This improved training consistency significantly.

# 5. Training Setup  

## Hyperparameters:

- Loss function: Cross-Entropy Loss  
- Optimizer: Adam  
- Learning rate: 0.001 (tuned experimentally)  
- Batch size: 32  
- Epochs: 15–30  
- Train/Validation split: 80% / 10% / 10%  

## Training strategy:
- Early stopping based on validation loss  
- Model checkpointing for best weights  

# 6. Evaluation Metrics  

The following metrics were used:

- Accuracy  
- Precision (macro average)  
- Recall (macro average)  
- F1-score  
- Confusion matrix  

These metrics ensure fair evaluation across all classes.

# 7. Results and Comparison  

## 7.1 Final Results Table  

| Model | Accuracy | Precision | Recall | F1-score | Training Behavior |
|------|----------|-----------|--------|----------|-------------------|
| CNN | **0.78 – 0.85** | High | High | High | Stable convergence |
| MLP | **0.52 – 0.65** | Medium | Low | Low | Fast but unstable |


## 7.2 Training Behavior Observations  

### CNN:
- Smooth decrease in loss  
- Stable validation accuracy  
- Less overfitting due to augmentation + BatchNorm  

### MLP:
- Quick convergence but poor generalization  
- High validation loss compared to training loss  
- Overfitting on training data  

## 7.3 Key Insight  

CNN significantly outperforms MLP because:

- CNN captures spatial features  
- MLP treats images as flat vectors  
- CNN learns hierarchical patterns  

# 8. Error Analysis  

The CNN model made mistakes in cases such as:

## 8.1 Common Confusions:
- Mountain vs Glacier (similar textures)  
- Sea vs Street (lighting confusion)  
- Forest vs Mountain (background overlap)  

## 8.2 Causes of Errors:
- High visual similarity between classes  
- Low image quality in some samples  
- Lack of contextual information  

## 8.3 Confusion Matrix Insight:
Most errors occur between visually similar natural classes.

# 9. Limitations  

- Model trained from scratch (no transfer learning)  
- Limited computational power  
- Fixed image resolution (loss of fine details)  
- No ensemble methods used  
- Class similarity affects performance  

# 10. Conclusion  

This project successfully demonstrates the effectiveness of deep learning for image classification.

## Key conclusions:

- CNN is significantly more powerful than MLP for image tasks  
- Spatial feature learning is essential for vision problems  
- Batch Normalization improves training stability and convergence  
- Data augmentation reduces overfitting and improves generalization  

### Final takeaway:
> CNN-based architectures are the most suitable approach for real-world image classification tasks compared to fully connected networks.


# 11. References  

- Intel Image Classification Dataset (Kaggle)  
https://www.kaggle.com/datasets/puneet6060/intel-image-classification  

- TensorFlow Documentation  
https://www.tensorflow.org/  

- Keras Documentation  
https://keras.io/  

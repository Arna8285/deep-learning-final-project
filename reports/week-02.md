## Objective of Week 2  
The main goal of this week was to set up the dataset pipeline and implement initial models for image classification.

## Work Completed  

### 1. Dataset Preparation  
- Downloaded Intel Image Classification dataset from Kaggle  
- Extracted dataset into train/test folders  
- Organized data into structured directories:
  - training set  
  - validation set  
  - test set  

### 2. Data Preprocessing  
- Resized all images to a fixed input size  
- Normalized pixel values (0–1 scaling)  
- Applied basic preprocessing pipeline for CNN and MLP models  


### 3. Baseline Model (MLP Implementation)  
- Built a Multilayer Perceptron (MLP) model as a baseline  
- Flattened image input into 1D vectors  
- Trained model using Cross-Entropy Loss  
- Evaluated initial performance on validation set  


### 4. CNN Model Setup  
- Designed initial Convolutional Neural Network architecture  
- Added:
  - Convolutional layers  
  - Max Pooling layers  
  - Fully connected layers  
  - Dropout for regularization  
- Implemented training pipeline  


### 5. Batch Normalization (Initial Integration)  
- Added Batch Normalization layers into CNN  
- Observed improved training stability during early experiments  


## Initial Observations  
- MLP model showed limited performance due to lack of spatial feature learning  
- CNN performed significantly better even in early training stages  
- Batch Normalization helped reduce training instability  

## Next Steps (Week 3 Plan)  
- Improve CNN architecture (more layers / tuning)  
- Apply data augmentation  
- Tune hyperparameters (learning rate, batch size)  
- Compare CNN vs MLP more formally using metrics  

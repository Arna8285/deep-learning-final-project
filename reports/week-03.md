## Objective of Week 3  
The main goal of this week was to improve the CNN model, apply data augmentation, and perform a more structured comparison between CNN and MLP models.

## Work Completed  

### 1. Data Augmentation  
To improve generalization and reduce overfitting, the following augmentation techniques were applied:

- Horizontal flipping  
- Random rotation  
- Zooming  
- Slight image transformations  

These techniques increased dataset variability and helped the model learn more robust features.

### 2. CNN Model Improvements  
The CNN architecture was improved by:

- Adding additional convolutional layers  
- Improving feature extraction depth  
- Keeping Batch Normalization layers  
- Using Dropout for regularization  

These changes helped stabilize training and improve accuracy.

### 3. Training Optimization  
- Adjusted learning rate for better convergence  
- Tuned batch size for stable training  
- Monitored validation loss to reduce overfitting  

### 4. MLP vs CNN Experiment Setup  
A structured comparison was performed between:

- **MLP (baseline model)**  
- **CNN (improved model with Batch Normalization and augmentation)**  

Both models were trained under similar conditions to ensure fair comparison.

## Results and Observations  

### MLP Model  
- Fast training speed  
- Poor performance on complex image data  
- Unable to capture spatial features  

### CNN Model  
- Significantly higher accuracy than MLP  
- Better generalization on validation data  
- Batch Normalization improved training stability  
- Data augmentation reduced overfitting  


## Key Insight  
CNN clearly outperforms MLP in image classification tasks because it can learn spatial and hierarchical features, while MLP treats images as flat vectors.


## Next Steps (Week 4 Plan)  
- Final evaluation of models on test set  
- Generate final performance metrics (accuracy, precision, recall, F1-score)  
- Visualize results (loss/accuracy graphs)  
- Prepare final report and conclusion  

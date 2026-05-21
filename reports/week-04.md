## Objective of Week 4  
The main goal of this week was to finalize model evaluation, compare CNN and MLP performance, visualize results, and complete the project report.

## Work Completed  

### 1. Final Model Evaluation  
Both models were evaluated on the test dataset using the following metrics:

- Accuracy  
- Precision  
- Recall  
- F1-score  

The evaluation was performed to measure real-world performance on unseen data.

### 2. CNN Final Performance  
The CNN model achieved strong results due to:

- Effective feature extraction using convolutional layers  
- Improved training stability from Batch Normalization  
- Reduced overfitting using Dropout and data augmentation  

Overall, CNN showed strong generalization ability.


### 3. MLP Final Performance  
The MLP model served as a baseline and showed:

- Faster but less accurate training  
- Poor performance on complex image patterns  
- Lack of spatial feature learning  

This confirmed that MLP is not suitable for image classification tasks compared to CNN.

### 4. Model Comparison Summary  

| Model | Performance | Observation |
|------|------------|------------|
| CNN | High accuracy (~70–85%) | Best performance, strong generalization |
| MLP | Lower accuracy | Limited by lack of spatial feature extraction |


### 5. Visualization of Results  
The following plots were analyzed:

- Training vs validation accuracy  
- Training vs validation loss  
- Performance comparison between CNN and MLP  

These visualizations confirmed that CNN converges more effectively and generalizes better.


## Key Findings  
- CNN significantly outperforms MLP in image classification tasks  
- Batch Normalization improves training stability and convergence speed  
- Data augmentation helps reduce overfitting and improves generalization  
- MLP is only suitable as a baseline model  


## Final Conclusion  
This project demonstrates the effectiveness of Convolutional Neural Networks for real-world image classification tasks.

CNN models are able to learn spatial and hierarchical features, making them far superior to MLP models for image-based problems.

Batch Normalization and data augmentation further improve performance and stability, resulting in a robust deep learning pipeline.


## Project Outcome  
- Successfully built CNN and MLP models  
- Performed structured comparison  
- Achieved expected accuracy range (70–85% for CNN)  
- Completed full deep learning pipeline from preprocessing to evaluation  

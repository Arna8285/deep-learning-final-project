# Dataset Report — Intel Image Classification Dataset

For this project, I selected the **Intel Image Classification Dataset** from **Kaggle**.  
Dataset source:  
https://www.kaggle.com/datasets/puneet6060/intel-image-classification/data

This dataset is widely used in computer vision and deep learning tasks, especially for image classification using Convolutional Neural Networks (CNNs).

The dataset contains approximately **25,000 color images** of real-world natural scenes collected from different environments around the world. All images are resized to **150 × 150 pixels**, which makes the dataset suitable for deep learning models while keeping computational cost manageable.

## Dataset Categories

The main objective of the dataset is to classify scene images into one of six categories:

1. **Buildings** — images containing houses, towers, and other man-made structures  
2. **Forest** — images of trees, forests, and green natural environments  
3. **Glacier** — images showing ice landscapes and snowy glaciers  
4. **Mountain** — images containing mountains and rocky landscapes  
5. **Sea** — images of oceans, beaches, and water scenes  
6. **Street** — urban street scenes with roads and city environments  

## Dataset Structure

The dataset is divided into three main parts:

- **Training Set (`seg_train`)** — around **14,000 images** used for training the CNN model  
- **Test Set (`seg_test`)** — around **3,000 images** used for evaluating model performance  
- **Prediction Set (`seg_pred`)** — around **7,000 unlabeled images** used for prediction and inference tasks  

The directory structure of the dataset is organized by class folders, which makes it compatible with popular deep learning frameworks such as **TensorFlow** and **PyTorch**. Each folder contains images belonging to a specific category.

## Dataset Complexity

This dataset is considered more challenging than beginner datasets such as **CIFAR-10** because it contains realistic outdoor scenes with variations in:

- lighting conditions  
- camera angles  
- object positions  
- weather conditions  
- background complexity  
- scene textures  

These challenges make the dataset appropriate for evaluating the performance of CNN architectures in real-world image classification tasks.

## Applications of the Dataset

The dataset is especially suitable for:

- Image Classification  
- Deep Learning research  
- CNN model training  
- Transfer Learning experiments  
- Computer Vision coursework  
- Multi-class classification tasks  

## Advantages of the Dataset

One of the major advantages of this dataset is that it provides balanced scene categories and enough image diversity to help neural networks learn meaningful visual features.

Additionally, the predefined train and test splits allow reproducible experiments and fair model evaluation.Suitable for comparing different deep learning models (CNN vs MLP)  

## Conclusion

Overall, the **Intel Image Classification Dataset** is an effective benchmark dataset for studying and implementing Convolutional Neural Networks (CNNs) on real-world scene recognition problems.

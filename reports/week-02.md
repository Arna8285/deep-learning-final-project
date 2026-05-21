## Completed Work
- Performed data preprocessing for the dataset.
- Resized and normalized images before training.
- Split the dataset into training, validation, and test sets.
- Built the baseline Convolutional Neural Network (CNN) model.
- Configured the training process, loss function, and optimizer.

## Data Preprocessing
The following preprocessing techniques were applied:
- Image resizing
- Normalization
- Conversion of images into tensors

Dataset split:
- 80% Training set
- 10% Validation set
- 10% Test set

## Baseline CNN Model
The initial CNN architecture includes:
- Convolutional layers
- ReLU activation functions
- MaxPooling layers
- Fully connected layers
- Softmax output layer

## Important Files / Commits
- Added preprocessing scripts
- Added dataset splitting code
- Implemented baseline CNN model
- Added initial training configuration

## Experiments Conducted
- Trained the baseline CNN model on the training dataset.
- Tested different batch sizes and learning rates.
- Evaluated initial model performance on validation data.

## Current Results
- The model successfully learned basic image features.
- Initial validation accuracy reached approximately 70%.
- Training process works correctly without major errors.

## Problems / Challenges
- Model shows signs of overfitting after several epochs.
- Training requires significant computation time.
- Hyperparameter tuning is still needed.

## Plan for Next Week
- Improve CNN architecture.
- Add regularization techniques:
  - Dropout
- Apply data augmentation techniques.
- Train the improved model and compare results.
- Generate performance graphs and error analysis.

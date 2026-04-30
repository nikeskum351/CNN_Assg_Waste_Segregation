# Waste Material Segregation Using CNN

A deep learning project that uses a Convolutional Neural Network (CNN) to classify waste images into material categories for better waste segregation and recycling support.

## Objective

The goal of this project is to build an image classification model that can automatically identify waste material types from images and classify them into one of the following 7 categories:

- Cardboard
- Food Waste
- Glass
- Metal
- Other
- Paper
- Plastic

## Dataset

- Total images: **7625**
- Number of classes: **7**
- Image size used for training: **224 × 224**
- Labels were derived from folder names in the dataset directory

## Project Workflow

### 1. Data Loading
- Loaded the dataset from the source directory
- Read images class-wise from folders
- Mapped folder names to class labels

### 2. Data Preprocessing
- Resized all images to **224 × 224**
- Converted images into array format
- Normalized pixel values using `1./255`
- Encoded class labels using label encoding and one-hot encoding

### 3. Data Visualization
- Plotted class distribution across all categories
- Displayed sample images from each waste type
- Verified image dimensions before training

### 4. Data Splitting
The dataset was divided into:
- **Training set:** 5340 images
- **Validation set:** 1141 images
- **Test set:** 1144 images

### 5. Model Building
A CNN model was built using:
- Convolution layers
- ReLU activation
- MaxPooling layers
- Dropout layers
- Dense layers
- Softmax output layer

### 6. Training Setup
- Optimizer: `adam`
- Loss function: `categorical_crossentropy`
- Metric: `accuracy`

### 7. Callbacks Used
- `EarlyStopping`
- `ReduceLROnPlateau`

### 8. Data Augmentation
To improve generalization, augmentation techniques such as rotation, shifting, shear, zoom, and horizontal flip were used.

## Best Model Configuration

The best-performing model used:

- 4 convolution layers
- Filters: `32, 64, 128, 128`
- Kernel size: `(3, 3)`
- Pool size: `(2, 2)`
- Activation: `relu`
- Dropout: `0.25` and `0.5`

## Results

### Performance
- Training Accuracy: **0.5650**
- Validation Accuracy: **0.5118**
- Test Accuracy: **0.55**
- Weighted F1-Score: **0.52**

### Observations
- Plastic showed the strongest recall
- Glass, Other, and Paper were frequently misclassified
- Class imbalance affected overall performance
- The model provides a reasonable baseline for waste classification

## Challenges

- Class imbalance across categories
- Visual similarity between some waste classes
- Moderate model performance with a basic CNN architecture

## Future Improvements

- Use transfer learning models such as ResNet, MobileNet, or EfficientNet
- Apply class balancing techniques
- Perform hyperparameter tuning
- Improve augmentation and regularization
- Experiment with deeper architectures

## Conclusion

This project demonstrates the use of CNNs for automated waste material classification. While the current model achieves moderate accuracy, it establishes a solid baseline for building smarter and more scalable waste segregation systems.

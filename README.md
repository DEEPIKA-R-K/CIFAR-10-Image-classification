# CIFAR-10 Image Classification Using TensorFlow

## Project Overview

This project builds a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify images from the CIFAR-10 dataset into 10 different categories.

The model uses convolutional layers, batch normalization, dropout, and data augmentation to improve image classification performance and reduce overfitting.

## Dataset

The CIFAR-10 dataset contains 60,000 color images of size 32 × 32 pixels, divided into 10 classes.

**Classes:** Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, and Truck.

- Training dataset: 45,000 images
- Validation dataset: 5,000 images
- Test dataset: 10,000 images

The images are normalized before being passed to the model.
```

## Training Setup

The project uses TensorFlow and Keras to train the CNN model.

- **Optimizer:** Adam
- **Loss function:** Categorical cross-entropy
- **Evaluation metric:** Accuracy
- **Batch size:** 64
- **Training epochs:** 10 by default
- **Learning rate:** Exponential decay schedule
- **Reproducibility:** Random seeds are set for Python, NumPy, and TensorFlow.

The dataset is loaded using TensorFlow/Keras and processed with the `tf.data` API.

The data pipeline includes:
- Image normalization
- Data augmentation
- Dataset shuffling
- Batch processing
- Prefetching for improved performance

## Model Design Decisions

### 1. Convolutional Layers

Convolutional layers extract important image features, such as edges, textures, and shapes.

### 2. Batch Normalization

Batch normalization helps stabilize and speed up training.

### 3. ReLU Activation

ReLU introduces non-linearity, allowing the model to learn complex image patterns.

### 4. Max Pooling

Max pooling reduces spatial dimensions while retaining important features.

### 5. Dropout

Dropout reduces overfitting by randomly disabling some units during training.

### 6. Data Augmentation

Random image transformations help the model generalize better to unseen images.

### 7. Global Average Pooling and Softmax

Global average pooling reduces the feature maps before classification. The final softmax layer produces probabilities for the 10 classes.

## How to Run the Code

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd cifar10_tensorflow_project
```

### Step 2: Create a Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Run the Project

```bash
python cifar10_classifier.py
```

The CIFAR-10 dataset will be downloaded automatically when the script first runs, if needed.

### Step 5: View Results

After training, the script evaluates the model on the test dataset and generates training and evaluation visualizations, including:

- Training and validation loss
- Training and validation accuracy
- Misclassified test images

The trained model checkpoint is saved for future use.

## Future Improvements

- Experiment with additional convolutional layers and filters.
- Tune hyperparameters to improve validation accuracy.
- Add residual connections.
- Compare different optimizers and learning-rate schedules.
- Improve generalization using data augmentation and regularization.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib

## Author

Deepika Ramasamy Kamalam


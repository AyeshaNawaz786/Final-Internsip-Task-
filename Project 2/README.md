
# Project 2: End-to-End Deep Learning Pipeline for Image Classification

## Overview

This project implements a complete Deep Learning pipeline for multi-class image classification using the Intel Image Classification Dataset. The objective is to classify natural scene images into six different categories using various neural network architectures and evaluate their performance.

The project covers the complete workflow from data preprocessing and augmentation to model training, evaluation, comparison, and prediction.

---

## Dataset

### Intel Image Classification Dataset

The dataset contains approximately 17,000 images divided into six categories:

* Buildings
* Forest
* Glacier
* Mountain
* Sea
* Street

### Dataset Structure

```text
seg_train/
    buildings/
    forest/
    glacier/
    mountain/
    sea/
    street/

seg_test/
    buildings/
    forest/
    glacier/
    mountain/
    sea/
    street/

seg_pred/
```

---

## Project Objectives

* Perform image preprocessing and augmentation
* Build a Feed Forward Neural Network (FNN)
* Develop a Basic Convolutional Neural Network (CNN)
* Design a Deep CNN architecture
* Apply Batch Normalization
* Apply Dropout Regularization
* Compare model performances
* Evaluate models using multiple metrics
* Generate predictions on unseen images
* Save the best-performing model

---

## Technologies Used

* Python
* TensorFlow 2.18
* Keras
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-Learn

---

## Data Preprocessing

The following preprocessing techniques were applied:

* Image Rescaling
* Image Augmentation
* Random Rotation
* Horizontal Flipping
* Zoom Transformation
* Train-Validation Split

Image Size:

```text
128 × 128
```

Batch Size:

```text
32
```

---

## Models Implemented

### 1. Feed Forward Neural Network (FNN)

Architecture:

* Flatten Layer
* Dense Layer (256)
* Dense Layer (128)
* Output Layer

Purpose:

* Baseline comparison model

---

### 2. Basic CNN

Architecture:

* Conv2D
* MaxPooling
* Conv2D
* MaxPooling
* Dense Layer
* Output Layer

Purpose:

* Feature extraction using convolution operations

---

### 3. Deep CNN

Architecture:

* Conv2D
* Batch Normalization
* MaxPooling
* Conv2D
* Batch Normalization
* MaxPooling
* Conv2D
* Batch Normalization
* MaxPooling
* Dropout
* Dense Layer
* Dropout
* Output Layer

Purpose:

* Improved feature extraction
* Better generalization
* Reduced overfitting

---

## Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

## Training Analysis

Training performance was analyzed through:

* Accuracy Curves
* Validation Accuracy Curves
* Loss Curves
* Validation Loss Curves

These visualizations helped monitor learning behavior and detect overfitting.

---

## Model Comparison

The final comparison includes:

| Model    | Validation Accuracy |
| -------- | ------------------- |
| FNN      | Evaluated           |
| CNN      | Evaluated           |
| Deep CNN | Evaluated           |

The Deep CNN achieved the best overall performance due to its deeper architecture, Batch Normalization, and Dropout regularization.

---

## Model Saving

The best-performing model is saved using:

```python
model.save("best_model.keras")
```

---

## Results

Key outcomes:

* Successful multi-class image classification
* Effective use of data augmentation
* Improved performance using Deep CNN
* Reduced overfitting with Dropout
* Stable learning through Batch Normalization
* Accurate predictions on unseen images

---

## Conclusion

This project demonstrates a complete Deep Learning workflow for image classification. Multiple neural network architectures were developed and compared. Experimental results showed that Deep CNN models outperform traditional Feed Forward Neural Networks by learning complex visual features directly from image data.

The implementation highlights the importance of convolutional layers, regularization techniques, and proper evaluation strategies in building robust image classification systems.

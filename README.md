# Vegetable/Non-Vegetable Binary Classifier

## Table of Contents
1. [Overview](#overview)
2. [Motivation](#motivation)
3. [Dataset](#dataset)
4. [Data Preprocessing](#data-preprocessing)
5. [Methodology](#methodology)
6. [Results](#results)

---

## Overview
This project develops a binary classifier to distinguish between vegetable and non-vegetable food items using computer vision techniques. The classifier leverages transfer learning with a fine-tuned ResNet50 model, making it robust for smaller datasets and reducing the risk of overfitting.

---

## Motivation
### Problem
The aim is to build a classifier capable of distinguishing between vegetarian and non-vegetarian food items.

### Why?
- To extend identifiable food classes for improved utility in applications.
- To address concerns related to allergies and dietary restrictions.
- To aid menu and recipe applications with better food classification.

---

## Dataset
### Public Datasets
The following public datasets were used:
- [Grocery Store Dataset](https://github.com/marcusklasson/GroceryStoreDataset/tree/master/dataset)
- [Food-11 Dataset](https://www.kaggle.com/datasets/trolukovich/food11-image-dataset)
- [Fruits and Vegetable Image Recognition Dataset](https://www.kaggle.com/datasets/kritikseth/fruit-and-vegetable-image-recognition)

### Our Dataset
- Video of food items recorded at the SoVi cafeteria at the University of North Carolina at Charlotte.
- Video frames were extracted into images using OpenCV for training.

---

## Data Preprocessing
- **Total Dataset:**
  - Non-Vegetarian: ~3500 images
  - Vegetarian: ~2500 images
- **Data Augmentation:**
  - Horizontal and vertical flipping to increase dataset size and diversity.
- **Data Normalization:**
  - Used PyTorch's `.Normalize()` function.
- **Train-Test Split:**
  - 20% of the training data was randomly selected as the test set.

---

## Methodology
### Model Architecture
- **Model:** Fine-Tuned ResNet50  
  - Chosen for its superior performance in image classification tasks.
  - Optimized for smaller datasets to prevent overfitting.

### Hyperparameters
- Image Size: `(64, 64)`
- Learning Rate: `0.001`
- Epochs: `10`
- Batch Size: `64`

### Evaluation Metrics
- **AUC (Area Under the ROC Curve):** Measures the classifier's performance.
- **Loss Function:** Binary Cross-Entropy With Logits Loss.

---

## Results
- **Final Accuracy:** `95.27%`
- **Final Training Loss:** `0.1658`
- **Final Average Loss:** `0.2729`
---

## Contributors
- **Daniel Santos** (Undergraduate)
- **Akhil Adusumilli** (Undergraduate)
- **James Holloway** (Undergraduate)

---

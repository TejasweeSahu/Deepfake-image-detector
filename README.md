# **Deepfake Image Detector**

A deepfake detection model built using image data and JSON predictions. This project is designed to train a robust predictive model that identifies whether an image is "real" or "fake" based on provided training data. The solution is scalable and generalizes effectively to unseen test images.

---

## **Table of Contents**
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Approach](#approach)
- [Model Architecture](#model-architecture)
- [Results](#results)

---

## **Problem Statement**
The goal of this project is to detect whether an image is a deepfake or not. The dataset consists of:
- **Training images** (real and fake).
- **JSON files** with predictions corresponding to the training images.
- **Test images** for which predictions are to be generated.

The objective is to build a model that predicts deepfake labels for test images and outputs the predictions in a specified JSON format.

---

## **Dataset**
- **Training Data**:
  - `fake_cifake_images`: Contains fake images.
  - `real_cifake_images`: Contains real images.
  - `fake_cifake_preds.json`: Contains labels (`fake`) for fake images.
  - `real_cifake_preds.json`: Contains labels (`real`) for real images.
- **Test Data**:
  - `test/`: Contains test images for which predictions need to be generated.

---

## **Approach**
1. **Data Preprocessing**:
   - Resized all images to `224x224`.
   - Normalized pixel values to [0, 1].
   - Converted labels in JSON files into a binary format (`0` for real, `1` for fake`).
2. **Model**:
   - Used a Convolutional Neural Network (CNN) for training.
   - Explored transfer learning with pre-trained models like ResNet for improved performance.
3. **Evaluation**:
   - Split the training data into training and validation sets.
   - Evaluated the model using accuracy and robustness metrics.
4. **Output**:
   - Predicted labels for test images.

## **Model Architecture**
The CNN architecture used:
- **Convolutional Layers**: For feature extraction.
- **Pooling Layers**: To reduce dimensionality.
- **Dropout**: To prevent overfitting.
- **Dense Layers**: For classification.

---

## **Results**
The model achieved:
- High accuracy(0.8696) on validation data.
- Robust predictions on unseen test data.



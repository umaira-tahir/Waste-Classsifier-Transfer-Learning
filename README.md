# 🗑️ Waste Classification Using Transfer Learning & Fine-Tuning

An image classification system that automatically categorizes waste into **Organic (O)** and **Recyclable (R)** using Convolutional Neural Networks, built with VGG16 Transfer Learning and Fine-Tuning in TensorFlow/Keras.

Developed as the final project for the **IBM AI Engineering Professional Certificate** (Deep Learning with Keras and TensorFlow course).

---

## 📌 Project Overview

Improper waste segregation is a major environmental challenge. This project builds a deep learning model that can automatically classify waste images into organic and recyclable categories, supporting smarter and more efficient waste management systems.

---

## 🏗️ Model Architecture & Approach

The project follows a two-stage transfer learning strategy using the **VGG16** pre-trained network:

1. **Feature Extraction Model**
   - VGG16 base (pre-trained on ImageNet) used as a frozen feature extractor.
   - Custom dense classification layers added on top.
   - Only the new top layers are trained.

2. **Fine-Tuned Model**
   - Top convolutional layers of VGG16 are unfrozen.
   - Model is retrained with a low learning rate to adapt pre-trained features to the waste classification task.
   - Achieves improved accuracy over the feature extraction model alone.

---

## 🧰 Tech Stack

- **Language:** Python
- **Deep Learning Framework:** TensorFlow, Keras
- **Pre-trained Model:** VGG16 (ImageNet weights)
- **Data Handling:** ImageDataGenerator (data augmentation & preprocessing)
- **Evaluation & Visualization:** Scikit-learn, Matplotlib
- **Environment:** Jupyter Notebook

---

## 📊 Workflow

1. **Data Preprocessing** — Image resizing, rescaling, and augmentation using `ImageDataGenerator`.
2. **Train/Validation/Test Split** — Organized into separate generators for training, validation, and testing.
3. **Feature Extraction** — Building and training a classifier on top of frozen VGG16 layers.
4. **Fine-Tuning** — Unfreezing top VGG16 layers and retraining with a low learning rate.
5. **Evaluation** — Accuracy/loss curves, classification report, and visual predictions on test images.

---

## 📈 Results

- Model performance evaluated using **accuracy and loss curves** for both the feature extraction and fine-tuned models.
- Fine-tuning improved classification accuracy compared to the feature extraction stage alone.
- Visual predictions on test images confirm the model's ability to correctly distinguish between Organic and Recyclable waste.

---

## 🚀 How to Run

1. Clone this repository.
2. Open `Final Proj-Classify Waste Products Using TL FT.ipynb` in Jupyter Notebook or Google Colab.
3. Install the required libraries:
   ```bash
   pip install tensorflow numpy scikit-learn matplotlib
4. Run all cells in order (Kernel → Restart & Run All).
5. View outputs including model summary, accuracy/loss curves, and test predictions.

---

## 🎓 Acknowledgment

This project was completed as part of the IBM AI Engineering Professional Certificate on Coursera, developed by IBM Skills Network.

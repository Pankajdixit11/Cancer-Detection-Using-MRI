# 🧠 Brain Tumor MRI Classification using CNN

An end-to-end Deep Learning project using **Convolutional Neural Networks (CNN)** and **TensorFlow/Keras** to detect and classify brain tumors from MRI scans into four distinct categories: **Glioma, Meningioma, Pituitary, and No Tumor**.

---

## 📌 Features

* **Automatic Dataset Download:** Integrates `kagglehub` to fetch the dataset directly into python scripts without manual downloading.
* **Data Augmentation:** Includes rotation, zoom, and horizontal flip transformations to mitigate overfitting.
* **Custom CNN Architecture:** Uses `Conv2D`, `BatchNormalization`, `MaxPooling2D`, and `Dropout` layers for robust feature extraction.
* **Comprehensive Evaluation:** Generates Accuracy/Loss curves, Classification Reports (Precision, Recall, F1-Score), and Confusion Matrices.

---

## 🗂️ Dataset

This project uses the **Brain Tumor MRI Dataset** available on Kaggle:
* **Dataset Link:** [Brain Tumor MRI Dataset (Sartaj Bhuvaji)](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri)

### Classes Identified:
1. `glioma`
2. `meningioma`
3. `notumor`
4. `pituitary`

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/brain-tumor-mri-classification.git](https://github.com/your-username/brain-tumor-mri-classification.git)
cd brain-tumor-mri-classification
```
## 🚀 How to Run
bash
python train.py

## 🧱 Model Architecture
```
Input (150x150x3) 
  │
  ├── Rescaling (1./255)
  ├── Random Augmentations (Flip, Rotation, Zoom)
  │
  ├── Conv2D (32 filters, 3x3) -> BatchNormalization -> MaxPooling2D
  ├── Conv2D (64 filters, 3x3) -> BatchNormalization -> MaxPooling2D
  ├── Conv2D (128 filters, 3x3) -> BatchNormalization -> MaxPooling2D
  ├── Conv2D (128 filters, 3x3) -> BatchNormalization -> MaxPooling2D
  │
  ├── Flatten
  ├── Dense (256, ReLU) -> Dropout (0.5)
  └── Dense (4, Softmax) -> Output
```

### 📜 License
---

<FollowUp label="Want me to add a custom badges section (Python, TensorFlow, License) or license file to this README?" query="Add badge headers and license details to the Brain Tumor MRI GitHub README file."/>


## Conclusion
This project demonstrates an end-to-end deep learning pipeline for automated brain tumor classification using MRI scans. By applying a custom Convolutional Neural Network (CNN) with built-in data augmentation, batch normalization, and dropout regularization, the model effectively categorizes scans into four distinct classes (glioma, meningioma, notumor, and pituitary).

The integrated pipeline streamlines medical image preprocessing, model training, and performance evaluation, providing an accurate, reliable, and non-invasive computer-aided diagnostic tool to assist clinical decision-making.

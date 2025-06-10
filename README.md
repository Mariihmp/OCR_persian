# Persian OCR using LeNet5 (Character-Level OCR)
با استفاده از LeNet5 (تشخیص کاراکتر در سطح کلمه)

---

##  Introduction
Optical Character Recognition (OCR) has become a key technology for converting images containing printed or handwritten text into machine-encoded text. This project focuses on **Persian OCR**, targeting Persian alphabets and digits.

The model is based on **LeNet5**, a well-known convolutional neural network (CNN) architecture adapted for Persian text. It provides a robust solution for recognizing Persian characters in images.

> این پروژه شامل بیش از 570,000 تصویر برچسب‌گذاری‌شده از حروف و ارقام فارسی است که شامل تصاویر تکی و توالی کاراکترها (مانند کلمات یا اعداد) می‌باشد.

---

##  Dataset

The OCR system is trained on a publicly available dataset with approximately **570,000 labeled grayscale images** of size **32x32**.

- **Characters**: 32 Persian letters, 10 digits, and additional symbols.
- **Access**: You can find the dataset on Kaggle.
- **Format**: Grayscale, 32x32 pixels, single-channel.

---

##  Preprocessing

Before feeding the images to the model, they undergo several preprocessing steps:

- Resizing all images to **32x32** pixels
- Normalizing pixel values to a **0–1** range
- Label encoding for classification

> تغییر اندازه و نرمال‌سازی باعث پایداری بیشتر مدل و بهبود عملکرد یادگیری می‌شود.

---

## Architecture – LeNet5

This project uses the **LeNet5 CNN** architecture, ideal for image classification tasks such as digit or character recognition.

### LeNet5 Layer Breakdown:
- **Input Layer**: 32x32 grayscale image
- **Conv Layer 1**: 6 filters (5x5) → 28x28 feature maps
- **MaxPooling 1**: 2x2 → 14x14 feature maps
- **Conv Layer 2**: 16 filters (5x5) → 10x10
- **MaxPooling 2**: 2x2 → 5x5
- **Fully Connected 1**: 120 units
- **Fully Connected 2**: 84 units
- **Output Layer**: Softmax (for 32 Persian characters + 10 digits)

---

## Model Performance

After training on the dataset and testing on a separate test set:

| Metric    | Value   |
|-----------|---------|
| Accuracy  | 91.0%   |
| Precision | 90.2%   |
| Recall    | 89.5%   |
| F1-Score  | 89.8%   |

---

##  How to Run in Test Mode (Character Prediction)

You can evaluate the trained model on new unseen images using the pipeline:
On test model.ipynb notebook by feeding image to pipeline we can get the result prediciton 

### 1. Install Requirements

```bash
pip install tensorflow numpy opencv-python matplotlib



Persian OCR using LeNet5
This repository contains code for building an Optical Character Recognition (OCR) system designed specifically for recognizing Persian alphabets and numbers. The system utilizes the LeNet5 architecture, a classic convolutional neural network (CNN) that is widely used for image recognition tasks.

Table of Contents
Introduction

Dataset

Accuracy

Architecture

Installation

Usage

Training the Model

Pretrained Models

Evaluation

License

Acknowledgments

Introduction
Optical Character Recognition (OCR) has become a key technology for converting images containing printed or handwritten text into machine-encoded text. This project focuses on Persian OCR, targeting Persian alphabets and digits. The model is based on LeNet5, which is a well-known convolutional neural network (CNN) architecture that has proven successful in image classification tasks. It has been adapted here to work with Persian text, making it a robust solution for text recognition in Persian scripts.

Dataset
The OCR system is trained on a publicly available dataset containing approximately 570,000 labeled images of Persian alphabets and digits. The dataset includes both single-character images and character sequences that represent Persian words and numbers.

You can access the dataset on Kaggle via the following link:
Persian Alphabets and Numbers Dataset

Dataset Overview
Number of images: 570,000

Categories: Persian alphabets (32 characters), numbers (10 digits), and other characters.

Image dimensions: 32x32 pixels, grayscale.

Preprocessing
The dataset images are preprocessed before feeding them into the model. Preprocessing includes:

Resizing the images to a consistent size (32x32 pixels).

Normalization of pixel values to a range of 0-1 for model stability.

Label encoding for categorical classification.

Accuracy
After training the model on the provided dataset, the OCR system achieves an accuracy of around 91% on classification tasks. This is based on evaluating the model on a separate test set, which was not part of the training data.

Performance Metrics
Accuracy: 91%

Precision: 90.2%

Recall: 89.5%

F1-Score: 89.8%

Architecture
The OCR model is built using the LeNet5 architecture. LeNet5 is a pioneering CNN architecture that has been successfully applied to handwritten digit recognition (such as the MNIST dataset) and is well-suited for similar tasks, including Persian text recognition.

LeNet5 Architecture Breakdown:
Input Layer: 32x32 grayscale image.

Convolutional Layer 1: 6 filters of size 5x5, producing 6 feature maps of size 28x28.

Pooling Layer 1: Max pooling with a 2x2 window, producing 6 feature maps of size 14x14.

Convolutional Layer 2: 16 filters of size 5x5, producing 16 feature maps of size 10x10.

Pooling Layer 2: Max pooling with a 2x2 window, producing 16 feature maps of size 5x5.

Fully Connected Layer 1: 120 units.

Fully Connected Layer 2: 84 units.

Output Layer: Softmax layer for 32 character classes (Persian alphabet) + 10 digits.

The architecture's key strengths are its simplicity, efficiency, and proven performance in image recognition tasks.
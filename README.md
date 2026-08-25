# UG-MSCST Brain Tumor Classification

## Overview

This repository contains the implementation of a deep learning-based brain tumor classification system using MRI brain images.

The project aims to classify brain MRI images into multiple tumor categories using a Convolutional Neural Network (CNN).

## Project Objective

The objective of this work is to develop an automated image classification approach that can assist in identifying different types of brain tumors from MRI images.

## Dataset

The dataset contains MRI images belonging to four classes.

- Training images: 5,600
- Validation images: 1,120
- Testing images: 1,600
- Number of classes: 4

The dataset is divided into training, validation, and testing sets for model development and evaluation.

## Methodology

The general workflow of the project is:

1. MRI image dataset collection
2. Image preprocessing
3. Dataset splitting
4. CNN model development
5. Model training
6. Validation
7. Testing
8. Performance evaluation

## Model

A Convolutional Neural Network (CNN) is used as the baseline deep learning model for multi-class brain tumor classification.

The baseline model was trained for 25 epochs.

## Results

The baseline CNN model achieved a test accuracy of approximately:

**46.56%**

The results can be further improved through advanced preprocessing, data augmentation, transfer learning, hyperparameter optimization, and improved CNN architectures.

## Repository Contents

```text
UG-MSCST-Brain-Tumor-Classification/
│
├── brain_tumor_classification.py.ipynb
└── README.md

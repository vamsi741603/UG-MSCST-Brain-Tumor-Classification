# UG-MSCST Brain Tumor Classification

## 📌 Overview

Brain tumor classification from Magnetic Resonance Imaging (MRI) scans is an important computer vision and medical imaging research problem. Accurate classification can support automated analysis of MRI images and assist researchers in developing computer-aided diagnostic systems.

This project presents a deep learning-based approach for multi-class brain tumor image classification using a Convolutional Neural Network (CNN). The system processes MRI brain images and classifies them into four categories: **Glioma, Meningioma, No Tumor, and Pituitary**.

The implemented workflow includes image preprocessing, dataset preparation, CNN-based model training, validation, and performance evaluation using multiple metrics. The model evaluation reported an **accuracy of 95.31%**, **precision of 95.67%**, **recall of 95.31%**, **F1-score of 95.21%**, and **ROC-AUC of 98.61%**.

This repository provides the implementation and documentation required to reproduce and further develop the experimental work presented in the associated academic research project.


## 🎯 Objectives

The main objectives of this project are:

1. To develop an automated brain tumor classification system using MRI images.
2. To preprocess and prepare MRI images for deep learning.
3. To train a CNN model for multi-class classification.
4. To evaluate the trained model using an independent test dataset.
5. To analyze the classification performance using suitable evaluation metrics.
6. To provide a reproducible implementation for academic and research purposes.

---

## 🧠 Classification Classes

The model classifies MRI images into four categories:

| Class          | Description                               |
| -------------- | ----------------------------------------- |
| **Glioma**     | Brain tumor originating from glial cells  |
| **Meningioma** | Tumor arising from the meninges           |
| **Pituitary**  | Tumor associated with the pituitary gland |
| **Normal**     | MRI image without a detected tumor        |

---

## 📊 Dataset

The project uses a labeled MRI brain image dataset containing four classes:

* **Glioma**
* **Meningioma**
* **No Tumor**
* **Pituitary**

### Dataset Distribution

The original dataset contains **7,200 images**:

| Class          | Original Training Set | Testing Set |
| -------------- | --------------------: | ----------: |
| **Glioma**     |                 1,400 |         400 |
| **Meningioma** |                 1,400 |         400 |
| **No Tumor**   |                 1,400 |         400 |
| **Pituitary**  |                 1,400 |         400 |
| **Total**      |             **5,600** |   **1,600** |

The original training set of **5,600 images** is further divided for model development:

| Split          | Number of Images |
| -------------- | ---------------: |
| **Training**   |        **4,480** |
| **Validation** |        **1,120** |
| **Testing**    |        **1,600** |
| **Total**      |        **7,200** |

The dataset is used for model training, validation, and independent evaluation.

> **Note:** The dataset itself is not included in this repository. Users should obtain the dataset from its appropriate source and configure the dataset path before running the notebook.


## 🔬 Methodology

The overall workflow of the proposed system is:

```text
MRI Brain Image Dataset
          ↓
   Image Preprocessing
          ↓
      Data Splitting
          ↓
   CNN Model Development
          ↓
       Model Training
          ↓
      Validation
          ↓
       Model Testing
          ↓
 Performance Evaluation
          ↓
 Brain Tumor Classification
```

---

## ⚙️ Model Architecture

A Convolutional Neural Network (CNN) is used as the deep learning model for classifying MRI images.

The model learns hierarchical image features through convolutional and pooling operations and performs multi-class classification through fully connected layers.

The training configuration includes parameters such as:

* Image preprocessing
* Batch processing
* Dropout regularization
* Model checkpointing
* Multi-class classification
* Validation during training

The notebook contains the complete implementation and training procedure.

---

## 📈 Results

The developed deep learning model was evaluated using multiple performance and calibration metrics.

| Metric                               |     Result |
| ------------------------------------ | ---------: |
| **Accuracy**                         | **95.31%** |
| **Precision**                        | **95.67%** |
| **Recall**                           | **95.31%** |
| **F1-Score**                         | **95.21%** |
| **ROC-AUC**                          | **98.61%** |
| **Expected Calibration Error (ECE)** | **0.0444** |

These results indicate strong classification performance across the four MRI image categories. The ROC-AUC value of **98.61%** indicates strong discriminative performance, while the ECE value provides an indication of the model's probability calibration.

> **Note:** The reported values are taken from the evaluation results generated by the project notebook. Results may vary depending on dataset preparation, random initialization, software versions, and experimental configuration.

## 📊 Evaluation

The model performance is evaluated using multiple quantitative metrics, including:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Expected Calibration Error (ECE)

A **confusion matrix** is also generated in the project notebook to visualize the classification performance across the four categories:

* Glioma
* Meningioma
* No Tumor
* Pituitary

The confusion matrix provides class-wise insight into correct and incorrect predictions and helps identify potential confusion between tumor categories.

The complete evaluation plots and results are available in:

`brain_tumor_classification.ipynb`


## 💻 Technologies Used

The project is implemented using Python and commonly used machine learning and deep learning libraries.

### Programming Language

* Python

### Development Environment

* Google Colab
* Jupyter Notebook

### Libraries / Frameworks

* NumPy
* Pandas
* Matplotlib
* TensorFlow
* Keras
* OpenCV
* scikit-learn

---

## 📁 Repository Structure

```text
UG-MSCST-Brain-Tumor-Classification/
│
├── brain_tumor_classification.ipynb
├── README.md
└── .gitignore
```

### File Description

| File                               | Description                                                                  |
| ---------------------------------- | ---------------------------------------------------------------------------- |
| `brain_tumor_classification.ipynb` | Complete model implementation, training, validation, and evaluation notebook |
| `README.md`                        | Project documentation                                                        |
| `.gitignore`                       | Prevents unnecessary files from being committed                              |

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/UG-MSCST-Brain-Tumor-Classification.git
```

### 2. Open the notebook

Open:

```text
brain_tumor_classification.ipynb
```

using either:

* Google Colab
* Jupyter Notebook
* JupyterLab

### 3. Configure the dataset

The notebook currently uses a Google Colab/Google Drive dataset path.

Locate the dataset configuration:

```python
'data_dir': r'/content/drive/MyDrive/dataset'
```

Change this path according to the location of your dataset.

### 4. Mount Google Drive

When using Google Colab, the notebook includes Google Drive mounting functionality for accessing the dataset.

### 5. Run the notebook

Execute the notebook cells sequentially to:

1. Load the configuration.
2. Load the dataset.
3. Verify the dataset.
4. Preprocess the images.
5. Train the CNN model.
6. Validate the model.
7. Evaluate the model.
8. Generate performance results.

---

## 🔄 Reproducibility

For reproducible experiments:

* Use the same dataset split.
* Use the same preprocessing procedure.
* Use the configuration parameters provided in the notebook.
* Use the same model architecture.
* Record the Python and library versions used during experimentation.

Exact results may vary depending on the hardware, software versions, random initialization, and dataset preparation.

---

## ⚠️ Important Note

This repository is intended for **academic and research purposes**.

The model is **not a certified medical diagnostic system** and should not be used to make clinical decisions or replace evaluation by qualified medical professionals.

---

## 📚 Research Context

This implementation is part of an academic research project focused on automated brain tumor classification from MRI images using deep learning techniques.

The repository is provided to support transparency, reproducibility, experimentation, and further research.

---

## 👨‍💻 Author

**Vamsi Kalisetty**

Undergraduate Research Project
UG-MSCST – Brain Tumor Classification

---

## ⭐ Acknowledgement

This project makes use of open-source Python, machine learning, and deep learning technologies for academic research and experimentation.

---

## 📄 License

This repository currently does not specify a separate open-source license.

If this code is intended to be reused or redistributed publicly, an appropriate license can be added after confirming the terms associated with the dataset and research work.

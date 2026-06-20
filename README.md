# Hybrid CNN-XGBoost Framework for Weld Defect Classification

## Abstract

This project presents a hybrid CNN-XGBoost framework for weld defect classification, developed to improve automated weld quality inspection using deep learning and machine learning techniques. The framework leverages Convolutional Neural Networks (CNNs) for extracting discriminative visual features from weld images and employs XGBoost as a powerful classifier for defect categorization. The proposed approach aims to enhance classification accuracy while maintaining model interpretability through Explainable AI (XAI) techniques such as SHAP and Grad-CAM.

The study is based on the LoHi-WELD dataset and focuses on classifying multiple weld defect categories commonly encountered in industrial manufacturing environments.

---

## Introduction

Weld quality inspection is a critical process in manufacturing industries, where defects can significantly affect structural integrity and product reliability. Traditional inspection methods are often time-consuming, subjective, and dependent on expert knowledge.

To address these challenges, this project proposes a hybrid deep learning framework that combines:

* CNN-based deep feature extraction
* XGBoost-based defect classification
* Explainable AI techniques for model interpretation

The framework is designed to automatically identify weld defects from images and provide reliable predictions for industrial quality control applications.

---

## Objectives

* Develop an automated weld defect classification system.
* Extract meaningful visual features using CNN architectures.
* Improve classification performance using XGBoost.
* Analyze model decisions using SHAP and Grad-CAM.
* Evaluate performance on the LoHi-WELD dataset.
* Support industrial weld inspection and quality assurance processes.

---

## Dataset

This project utilizes the **LoHi-WELD Dataset**, a publicly available industrial weld defect dataset containing both high-resolution and low-resolution weld images.

### Dataset Download

**Google Drive Link:**
https://drive.google.com/file/d/1pXeEnREfV_MYcL5MY2vkd9njBm_blPUK/view

### Defect Categories

* Crack
* Pore
* Deposit
* Stain
* Normal Weld

### Dataset Split

* Training Set
* Validation Set
* Test Set

### Dataset Citation

If you use the LoHi-WELD dataset or any part of this implementation in your research, please cite the original dataset paper:

**IEEE Access Publication:**
https://www.mdpi.com/2673-4591/130/1/9

```bibtex
Pattabiraman, K.; Patil, A.; Gulavani, Y.; Malik, R.; Gai, A. An Efficient Hybrid Framework for Weld Defect Detection Using GAN, CNN and XGBoost. Eng. Proc. 2026, 130, 9. https://doi.org/10.3390/engproc2026130009


```

---

## Proposed Methodology

The proposed framework follows a hybrid learning pipeline:

### 1. Data Preprocessing

* Image resizing
* Normalization
* Data augmentation
* Dataset balancing

### 2. CNN-Based Feature Extraction

A convolutional neural network is trained to learn discriminative weld defect representations from input images. Deep features are extracted from the feature layer before classification.

### 3. XGBoost Classification

The extracted feature vectors are provided to an XGBoost classifier, which performs multi-class weld defect classification.

### 4. Explainable AI Analysis

To improve transparency and trustworthiness:

* **Grad-CAM** highlights image regions influencing predictions.
* **SHAP** explains feature contributions to classification decisions.

---

## System Architecture

```text
Input Weld Image
        │
        ▼
Image Preprocessing
        │
        ▼
CNN Feature Extraction
        │
        ▼
Deep Feature Vector
        │
        ▼
XGBoost Classifier
        │
        ▼
Defect Prediction
        │
        ▼
SHAP & Grad-CAM Analysis
```

---

## Project Structure

```text
Hybrid-CNN-XGBoost-Weld-Defect-Classification/
│
├── dataset/
├── preprocessing.py
├── cnn_model.py
├── feature_extraction.py
├── xgboost_classifier.py
├── train.py
├── evaluate.py
├── gradcam.py
├── shap_analysis.py
├── saved_models/
├── results/
├── requirements.txt
└── README.md
```

### Directory Description

* `dataset/` — LoHi-WELD dataset images
* `preprocessing.py` — image preprocessing and augmentation
* `cnn_model.py` — CNN architecture implementation
* `feature_extraction.py` — deep feature extraction module
* `xgboost_classifier.py` — XGBoost training and inference
* `train.py` — complete training pipeline
* `evaluate.py` — model evaluation metrics
* `gradcam.py` — Grad-CAM visualization
* `shap_analysis.py` — SHAP explainability analysis
* `saved_models/` — trained model files
* `results/` — plots, confusion matrices, and reports

---

## Technologies Used

* Python
* TensorFlow / Keras
* XGBoost
* OpenCV
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* SHAP

---

## Experimental Evaluation

The framework is evaluated using standard classification metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

Performance comparisons demonstrate the effectiveness of combining CNN feature extraction with XGBoost classification for weld defect recognition.

---

## Results and Discussion

The proposed hybrid framework achieved the following:

* Accurate classification of multiple weld defect categories.
* Improved feature representation through CNN-based learning.
* Enhanced classification performance using XGBoost.
* Better model interpretability through SHAP and Grad-CAM.
* Robust performance across both high-resolution and low-resolution weld images.

The results indicate that hybrid deep feature extraction and machine learning classification can provide an effective solution for automated weld inspection systems.

---

## Publication

This project is based on the research work published in:

**MDPI Engineering Proceedings**

**Paper Link:**
https://www.mdpi.com/2673-4591/130/1/9

Please refer to the publication for detailed methodology, experimental setup, and performance analysis.

---

## Future Work

* Real-time weld defect inspection systems
* YOLO-based defect localization and segmentation
* Edge AI deployment for industrial environments
* Transformer-based feature extraction architectures
* Integration with smart manufacturing and Industry 4.0 systems
* Automated weld quality monitoring platforms

---

## Acknowledgments

This work utilizes the **LoHi-WELD ****dataset** developed by:

* S.B. Block
* R.D. da Silva
* A.E. Lazzaretti
* R. Minetto

We gratefully acknowledge the authors for making the dataset publicly available and supporting research in automated weld defect detection and classification.

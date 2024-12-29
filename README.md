# **ECG Classification Using Linear Regression**
I developed a machine learning-based solution for ECG (Electrocardiogram) Classification using Linear Regression. This involves:  Identifying heartbeats as either Normal (0) or Abnormal (1) based on ECG signals.

An efficient system to classify ECG heartbeats into **Normal** or **Abnormal** categories using Linear Regression. This project provides a simple, interpretable, and reliable machine learning solution for detecting cardiac arrhythmias.

---

## **Table of Contents**
1. [Introduction](#introduction)  
2. [Features](#features)  
3. [Project Structure](#project-structure)  
4. [Dataset](#dataset)  
5. [Methodology](#methodology)  
6. [Results](#results)  
7. [Setup and Usage](#setup-and-usage)  
8. [Future Work](#future-work)  


---

## **Introduction**

Heart diseases are one of the leading causes of death worldwide. This project uses machine learning to classify heartbeats based on ECG signals into:  
- **Normal (0)**  
- **Abnormal (1)**  

The goal is to create a lightweight, easily deployable system that assists healthcare professionals in early detection and monitoring of heart conditions.

---

## **Features**

- **Classification**: Categorizes heartbeats as Normal or Abnormal.  
- **Visualization**: Displays performance metrics such as confusion matrix and ROC curve.  
- **Reusable Framework**: Includes modular functions for training, evaluating, and classifying ECG data.  

---

## **Project Structure**

```plaintext
ECG-Classification/
│
├── README.md                # Project overview and usage instructions
├── data/                    # Dataset files
│   ├── train_data.csv       # Training data
│   ├── test_data.csv        # Test data
│
├── src/                     # MATLAB source code
│   ├── ecg_classification.m # Main script
│   ├── classify_heartbeat_linear.m # Classify new ECG data
│   ├── normalize_features.m # Normalization function
│   ├── classify_label.m     # Labeling function
│
└── results/                 # Results from model evaluation
    ├── roc_curve.png        # Example ROC curve visualization
```
---

## **Dataset**

### **Source**  
- The dataset used is the [MIT-BIH Arrhythmia Dataset (preprocessed)](https://www.physionet.org/content/mitdb/1.0.0/).

### **Features and Labels**  
- **Features**: Numerical attributes derived from ECG signals.  
- **Labels**:  
  - `0` → Normal heartbeat.  
  - `1, 2, 3, 4` → Abnormal heartbeat (mapped to `1`).  

---

## **Methodology**

### **Data Preprocessing**  
- The ECG data is preprocessed by normalizing the features using **min-max scaling**.
- Labels are mapped into two categories: `0` for Normal and `1` for Abnormal (any abnormality is classified as `1`).

### **Model Training**  
- **Model Used**: Linear Regression.  
- The dataset is split into **80% training** and **20% testing**.
- The model is trained using the training set and evaluated on the test set.

### **Evaluation**  
- The model's performance is evaluated using:
  - **Accuracy**: Proportion of correct predictions.  
  - **Confusion Matrix**: To evaluate the types of errors (True Positives, False Positives, True Negatives, False Negatives).  
  - **ROC Curve**: To visualize the trade-off between sensitivity and specificity.  
  - **AUC**: Area under the ROC curve to assess the model's discriminatory power.

### **Prediction**  
- The trained model is used to predict whether heartbeats in new ECG data are Normal or Abnormal.

---

## **Results**

- **Accuracy**: 90.34%
  
- **Confusion Matrix**:  14185        235
                         1456        1635
  ---
## **Future Work
-Multi-class Classification: Extend the model to detect specific types of arrhythmia (e.g., atrial fibrillation, ventricular tachycardia).


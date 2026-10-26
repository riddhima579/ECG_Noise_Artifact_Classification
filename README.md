
# ECG Noise Artifact Classification

## Project Overview
This project focuses on classifying ECG noise artifacts using machine learning. It compares conventional statistical feature extraction with Discrete Wavelet Transform (DWT)-based feature extraction.

## Objectives
- Classify ECG signals into four categories.
- Compare DWT-based and conventional feature extraction.
- Evaluate Decision Tree, Random Forest, and Support Vector Machine (SVM) classifiers.
- Test model performance on an unseen ECG record.

## ECG Classes
1. Clean ECG
2. Baseline Wander
3. EMG Artifact
4. Motion Artifact

## Methodology
1. ECG data acquisition using the MIT-BIH Arrhythmia Database and MIT-BIH Noise Stress Test Database.
2. ECG segmentation into 5-second segments.
3. Addition and classification of noise artifacts.
4. Feature extraction using conventional statistical features and DWT.
5. Model training using Decision Tree, Random Forest, and SVM.
6. Performance evaluation using accuracy, precision, recall, F1-score, and confusion matrices.
7. External validation using an unseen ECG record.

## Feature Extraction
- Conventional statistical features: 11 features per segment.
- DWT-based features: db4 wavelet, Level 8, and 108 features per segment.

## Machine Learning Models
- Decision Tree
- Random Forest (200 trees)
- Support Vector Machine (SVM) with RBF kernel

## Results
DWT-based feature extraction performed better than conventional feature extraction in the reported experiments.

### Internal Evaluation — Record 118
| Classifier | DWT Accuracy | Conventional Accuracy |
|---|---:|---:|
| Decision Tree |  |  |
| Random Forest | 77.74% | 51.71% |
| SVM |  |  |

The remaining accuracy values can be added from the project results.

### External Validation — Record 119
| Classifier | DWT Accuracy | Conventional Accuracy |
|---|---:|---:|
| Decision Tree | 45.22% | 35.11% |
| Random Forest | 55.75% | 39.13% |
| SVM | 40.17% | 31.86% |

## Technologies Used
- Python
- Google Colab
- NumPy
- PyWavelets
- Scikit-learn
- Matplotlib
- WFDB

## Notebooks
The repository contains notebooks for DWT-based classification, conventional feature-based classification, and external validation.

## Dataset
The ECG data used in this project is available through PhysioNet:
- MIT-BIH Arrhythmia Database
- MIT-BIH Noise Stress Test Database

Obtain the datasets from their official sources and follow the applicable access and usage conditions. Dataset files are not included in this repository.

## Scope and Limitations
This project is intended for research and educational purposes. It is not a medical diagnostic system and is not intended for clinical use or live patient monitoring.

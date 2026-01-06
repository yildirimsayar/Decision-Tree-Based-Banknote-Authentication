# Decision-Tree-Based-Banknote-Authentication
This repository presents a machine learning project that focuses on classifying banknotes as authentic or forged using a Decision Tree Classifier trained on wavelet-transformed image features.

The project demonstrates how interpretable machine learning models can be effectively applied to real-world financial security problems.

Project Overview

Automated banknote authentication is a critical task in financial security systems.
In this project, a Decision Tree model is implemented and evaluated to distinguish between genuine and counterfeit banknotes based on statistical features extracted from images.

The work includes:

Data preprocessing and feature scaling

Baseline Decision Tree modeling

Model evaluation using accuracy and confusion matrices

Feature importance analysis

Decision tree structure visualization

Hyperparameter optimization using Grid Search

Dataset

Name: Banknote Authentication Dataset

Instances: 1,372

Features (Continuous):

Variance of Wavelet Transformed image

Skewness of Wavelet Transformed image

Curtosis of Wavelet Transformed image

Entropy of image

Target Variable:

Class (Authentic / Forged)

The features are derived from wavelet-transformed images of banknotes.

Methodology
Data Preprocessing

The dataset is split into training (70%) and testing (30%) subsets.

A fixed random seed is used to ensure reproducibility.

Standard Scaling (Z-score normalization) is applied.

The scaler is fitted only on the training data to prevent data leakage.

Model Implementation

A baseline Decision Tree model is trained using default hyperparameters.

Model performance is improved through hyperparameter tuning with GridSearchCV.

Different splitting criteria and tree depths are evaluated.

A pipeline is used to apply scaling consistently during cross-validation.

Evaluation

Classification accuracy

Confusion matrix analysis

Feature importance extraction

Decision tree visualization

Results
Model	Configuration	Accuracy
Baseline Model	Default Parameters (Gini)	98.06%
Optimized Model	Entropy, No Maximum Depth	99.27%

Key observations:

The Variance feature is the most influential factor in classification.

The baseline model achieves strong predictive performance.

Hyperparameter optimization further reduces misclassification.

The optimized model improves detection of forged banknotes.

Visual Analysis

The project includes multiple visualizations that support model interpretability:

Confusion matrices

Feature importance plots

Scatter plots showing feature separability

Decision Tree structure diagrams

These visual tools provide insight into how the model makes decisions.

Technologies Used

Python

Scikit-learn

NumPy

Pandas

Matplotlib

Conclusion

This project demonstrates that Decision Tree classifiers can deliver both high accuracy and interpretability in banknote authentication tasks.
With appropriate preprocessing and model tuning, the approach provides a reliable and transparent solution for detecting counterfeit banknotes.

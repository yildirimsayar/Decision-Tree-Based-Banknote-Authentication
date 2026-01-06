# Banknote Authentication using Decision Tree

This repository presents a machine learning project focused on classifying banknotes as authentic or forged using a Decision Tree classifier trained on wavelet-transformed image features.

---

## Project Overview

Automated banknote authentication is a critical task in financial security systems.  
This project applies a Decision Tree model to distinguish genuine and counterfeit banknotes based on statistical features extracted from images.

The work includes:
- Data preprocessing and feature scaling
- Baseline Decision Tree modeling
- Model evaluation using accuracy and confusion matrices
- Feature importance analysis
- Decision tree structure visualization
- Hyperparameter optimization using Grid Search

---

## Dataset

- Name: Banknote Authentication Dataset
- Number of instances: 1,372
- Feature type: Continuous
- Features:
  - Variance of Wavelet Transformed image
  - Skewness of Wavelet Transformed image
  - Curtosis of Wavelet Transformed image
  - Entropy of image
- Target variable:
  - Class (Authentic / Forged)

The features are derived from wavelet-transformed images of banknotes.

---

## Methodology

### Data Preprocessing

- The dataset is split into training (70%) and testing (30%) subsets.
- A fixed random seed is used to ensure reproducibility.
- Standard Scaling (Z-score normalization) is applied.
- The scaler is fitted only on the training data to prevent data leakage.

### Model Implementation

- A baseline Decision Tree model is trained using default hyperparameters.
- Hyperparameter tuning is performed using GridSearchCV.
- The following parameters are evaluated:
  - Splitting criterion: gini, entropy
  - Maximum tree depth
- A pipeline is used to ensure consistent scaling during cross-validation.

### Evaluation

- Classification accuracy
- Confusion matrix analysis
- Feature importance extraction
- Decision tree visualization

---

## Results

| Model | Configuration | Accuracy |
|------|--------------|----------|
| Baseline Model | Default Parameters (Gini) | 98.06% |
| Optimized Model | Entropy, No Maximum Depth | 99.27% |

Key observations:
- The Variance feature is the most influential factor in classification.
- The baseline model achieves strong predictive performance.
- Hyperparameter optimization reduces misclassification.
- The optimized model improves detection of forged banknotes.

---

## Visual Analysis

The project includes visualizations that support model interpretability:
- Confusion matrices
- Feature importance plots
- Scatter plots illustrating feature separability
- Decision Tree structure diagrams

These visuals provide insight into how the model makes decisions.

---

## Technologies Used

- Python
- Scikit-learn
- NumPy
- Pandas
- Matplotlib

---

## Conclusion

This project demonstrates that Decision Tree classifiers can achieve both high accuracy and strong interpretability for banknote authentication tasks.  
With appropriate preprocessing and model tuning, the approach provides a reliable and transparent solution for counterfeit banknote detection.

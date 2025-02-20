# AdaBoost-BreastCancer
# AdaBoost Breast Cancer Classification

## Overview
This project implements **AdaBoost** for binary classification using the **breast cancer dataset** from scikit-learn. The goal is to explore the performance of AdaBoost, visualize accuracy trends, examine how sample weighting affects learning, and analyze the impact of noisy data.

## Features
- Loads and preprocesses the **Breast Cancer dataset**.
- Trains an **AdaBoost Classifier** with decision stumps as weak learners.
- Evaluates accuracy on both training and testing sets.
- Plots accuracy trends as the number of weak learners increases.
- Examines how misclassified examples gain higher weights.
- Introduces noise into the dataset and observes its impact on classification performance.

## Dataset
- The dataset is obtained from `sklearn.datasets.load_breast_cancer()`.
- It contains **30 features** extracted from digitized images of breast mass biopsies.
- The classification task is to predict whether a tumor is **malignant (1)** or **benign (0)**.

## Installation
Make sure you have **Python 3.x** installed along with the required dependencies.

```bash
pip install numpy matplotlib scikit-learn
```

## Usage
Run the following command to execute the script:
```bash
python adaboost_breast_cancer.py
```

## Code Explanation
### 1. Load and Split Data
- The dataset is split into **80% training** and **20% testing** using `train_test_split`.

### 2. Train an AdaBoost Classifier
- The model is trained using `AdaBoostClassifier` with **decision stumps** (depth = 1).

### 3. Visualize Performance
- A **line plot** is generated to show accuracy trends as the number of weak learners (`n_estimators`) increases.

### 4. Explore Sample Weighting
- The weights of the first **10 weak learners** are displayed to observe how the model adjusts to misclassified samples.

### 5. Experiment with Noisy Data
- **10% of training labels** are randomly flipped to introduce noise.
- The model is retrained, and the accuracy with noisy data is compared to the original model.

## Results
- **Higher `n_estimators` generally improves accuracy**, but too many weak learners may lead to overfitting.
- **Misclassified samples receive higher weights**, influencing subsequent weak learners.
- **Noisy data reduces accuracy**, demonstrating AdaBoost’s sensitivity to label noise.

## Visualization Example
A plot is generated showing training and testing accuracy across different numbers of estimators.

![Performance Plot](performance_plot.png)

## License
This project is licensed under the **MIT License**.

---



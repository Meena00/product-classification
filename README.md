# Product Quality Classification Using Decision Trees

## Overview

This project builds a **Decision Tree classification model** to predict wine quality using physicochemical properties of red wine. The objective is to determine whether a wine falls into a **low quality** or **high quality** category based on measurable chemical characteristics such as acidity, density, and alcohol content.

The project demonstrates a basic machine learning workflow that includes **data preprocessing, model training, evaluation, and visualization**.

The dataset used for this analysis comes from the **UCI Machine Learning Repository Wine Quality dataset**.

---

## Dataset

The dataset contains laboratory measurements for red wine samples. Each row represents one wine observation along with several chemical attributes.

Dataset source:  
https://archive.ics.uci.edu/ml/datasets/Wine+Quality

### Input Features

The following variables were used as predictors in the model:

- **fixed_acidity**
- **volatile_acidity**
- **residual_sugar**
- **density**
- **pH**
- **alcohol**

### Target Variable

Wine quality scores in the dataset originally range from **0–10**.

To simplify the classification task, the scores were grouped into two categories:

- **0 – Low Quality** (original scores 3–6)
- **1 – High Quality** (original scores 7–10)

This converts the problem into a **binary classification task**.

---

## Project Workflow

### 1. Data Preprocessing

Several preprocessing steps were applied before building the model:

- Loaded the dataset using **Pandas**
- Converted the wine quality scores into binary categories
- Selected relevant feature columns for the model
- Split the dataset into **training and testing sets**
- Standardized feature values using **StandardScaler**

---

### 2. Model Training

A **Decision Tree Classifier** from `scikit-learn` was used to train the model.

The algorithm learns patterns in the training dataset and creates a tree structure that separates observations based on feature values.

---

### 3. Model Evaluation

The model was evaluated using standard classification metrics including:

- **Accuracy Score**
- **Confusion Matrix**
- **Classification Report**

These metrics provide insight into how well the model predicts wine quality categories.

---

### 4. Model Complexity Analysis

To better understand how tree depth affects performance, the model was trained using different **max_depth** values.

Testing multiple depths helps observe how model complexity impacts accuracy and whether deeper trees lead to overfitting.

---

## Decision Tree Visualization

The trained decision tree was visualized using `plot_tree` from scikit-learn.

The visualization illustrates:

- the sequence of decision splits
- which features influence classification
- how the model separates low and high quality wines

![Decision Tree](decisiontree.png)

---

## Technologies Used

- **Python**
- **NumPy**
- **Pandas**
- **Scikit-learn**
- **Matplotlib**

---
## Key Concepts Demonstrated

This project highlights several important machine learning concepts:

- data preprocessing and preparation  
- feature selection for classification  
- decision tree modeling  
- model evaluation using classification metrics  
- visualization of model decision structure  

These techniques form a foundation for many **data analysis and predictive modeling tasks**..

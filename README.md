# neural-network-challenge-2
This repository describes the building of a neural network model that can predict employee attrition and employee fit to their assigned roles.
# Employee Attrition Prediction

## Overview
This project involves predicting employee attrition and department using machine learning techniques.  The provided dataset is preprocessed to create and compile a deep learning model, and then the model's performance is evaluated based on the accuracy of its predictions. The goal is to develop a model that predicts whether an employee will leave the company (attrition) and, if so, their department, using various employee attributes.

## Project Structure

- `data/` –  input dataset in CSV format.
- `notebook/` – The Colab notebook containing the code for data preprocessing, model building, and evaluation.
- `README.md` – This file.

## Key Steps in the Process

### 1. **Data Preprocessing**
The following steps were performed to preprocess the data:
- Imported and viewed the first few rows of the dataset to understand its structure.
- Determined the number of unique values in each column to assess potential categorical variables.
- Split the dataset into features (`X`) and targets (`y`), where `y` contains the **attrition** and **department** columns.
- Selected at least 10 features for the model (`X_df`).
- Converted categorical columns to numeric format using encoders and scaled numerical features using **StandardScaler**.

### 2. **Model Creation and Training**
I created a **multi-output deep learning model** using Keras. The model has two branches:
- **Branch 1**: Predicts employee **attrition** (binary classification: `Yes/No`).
- **Branch 2**: Predicts the employee's **department** (multi-class classification).

The model was trained on the preprocessed data and evaluated on a test set.

### 3. **Evaluation**
After training, the model's performance was evaluated using **accuracy** as the primary metric. Accuracy for both the attrition and department predictions was reported.

## Key Points as Summary responses to Challenge Questions

- **Accuracy** may not be the best evaluation metric, especially in cases of class imbalance. Other metrics such as **precision**, **recall**, or **F1-score** may be more useful for understanding the model's performance.
- The **sigmoid activation function** was chosen for both output layers, suitable for binary classification tasks. 
- Possible improvements include **hyperparameter tuning**, **cross-validation**, and experimenting with more complex models like **decision trees** or **random forests**.

## Requirements

- Python 3.x
- Required libraries:
  - TensorFlow (for deep learning)
  - pandas (for data manipulation)
  - numpy (for numerical operations)
  - scikit-learn (for preprocessing and evaluation metrics)
  - matplotlib and seaborn (for visualizations, if applicable)

All of the above required libraries can be installed using `pip`:

```bash
pip install tensorflow pandas numpy scikit-learn matplotlib seaborn

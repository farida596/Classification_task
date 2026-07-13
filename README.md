# Titanic Survival Prediction Using Machine Learning

## Overview

This project builds and evaluates machine learning models to predict whether a passenger survived the Titanic disaster.

The workflow includes loading the dataset, preprocessing the data, handling missing values, encoding categorical variables, training classification models, and comparing their performance using multiple evaluation metrics.

---

## Dataset

- **Dataset:** Titanic Dataset
- **Source File:** `archive.zip`
- **Records:** 891 passengers
- **Target Variable:** `Survived`

---

## Project Workflow

### 1. Import Required Libraries

The project uses the following Python libraries:

- Pandas
- ZipFile
- Scikit-learn

---

### 2. Load the Dataset

The dataset is extracted from a ZIP file and loaded into a Pandas DataFrame.

---

### 3. Explore the Dataset

Before building the models, the dataset is inspected by checking:

- Dataset information
- Data types
- Missing values
- Dataset structure

---

### 4. Data Preprocessing

Several preprocessing steps are applied to prepare the data for machine learning.

#### Remove Unnecessary Columns

The following columns are removed because they do not contribute significantly to prediction:

- PassengerId
- Name
- Ticket
- Cabin

#### Handle Missing Values

- Missing values in **Age** are replaced with the column mean.
- Missing values in **Embarked** are replaced with the most frequent value (mode).

#### Encode Categorical Variables

Machine learning models require numerical input, so categorical features are converted into numerical values using one-hot encoding.

The following columns are encoded:

- Sex
- Embarked

---

### 5. Split the Dataset

The cleaned dataset is divided into:

- **80% Training Data**
- **20% Testing Data**

using `train_test_split()`.

---

## Machine Learning Models

Two classification models are implemented and compared.

### Logistic Regression

A Logistic Regression model is trained using the training dataset and used to predict passenger survival.

### Decision Tree

A Decision Tree classifier is also trained using the same training and testing sets for comparison.

---

## Model Evaluation

Both models are evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1 Score

### Logistic Regression Results

| Metric | Score |
|---------|-------|
| Accuracy | **81.01%** |
| Precision | **78.57%** |
| Recall | **74.32%** |
| F1 Score | **76.39%** |

### Decision Tree Results

| Metric | Score |
|---------|-------|
| Accuracy | **79.33%** |
| Precision | **76.06%** |
| Recall | **72.97%** |
| F1 Score | **74.48%** |

---

## Conclusion

Both machine learning models successfully predicted passenger survival.

The **Logistic Regression** model achieved better performance across all evaluation metrics, making it the preferred model for this dataset.

The model's performance could be further improved by:

- Feature engineering
- Hyperparameter tuning
- Trying ensemble methods such as Random Forest or Gradient Boosting

---

## Project Structure

```
├── Titanic_Survival_Prediction.ipynb
├── archive.zip
└── README.md
```

---
## Technologies Used

- Python
- Pandas
- Scikit-learn
- Jupyter Notebook

---

## Skills Demonstrated

This project demonstrates practical experience with:

- Data preprocessing
- Handling missing values
- Feature selection
- Categorical data encoding
- Train-test splitting
- Logistic Regression
- Decision Tree Classification
- Model evaluation
- Performance comparison

---



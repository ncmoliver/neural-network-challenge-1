# Student Loan Repayment Model

![logo of project file](/logo.png)

## Project Overview

The project aims to determine if a student will repay their student loan based on credit ranking, to ultimately calculate an accurate interest rate.

## Dataset

The dataset can be downloaded here --> [student loan project dataset](https://static.bc-edx.com/ai/ail-v-1-0/m18/lms/datasets/student-loans.csv)

### Files Included

- student_loans_with_deep_learning.ipynb
  - The jupyter notebook containing the entire project, from data preprocessing to the model evaluation.

## Project Steps

### Prerequisites

- Python (version 3.7 or higher)
- Google Collab (recommended)
- Libraries: Pandas,Scikit-learn,TensorFlow, Keras

## Data Preparation

1. Features (X), Target (y):
   - Features (X): All columns except for `credit_ranking`
   - Target (y): `credit_ranking` column
2. Split the data using `train_test_split`.
3. Scaled the data using `StandardScaler`.

## Model Steps

#### Model Design

- Use of TensorFlow to build neural network model.
- The model has 2 hidden layers and 1 output layer.

#### Model Compilation and Training

- Compiled the model with an appropiate loss function (`binary_crossentropy`) for the model to measure itself, and optimizer (`adam`).
- Train the model using the training data and evaluate the model using testing data (new data,
  data it has never seen).

## Model Evaluation

#### Results - Training Data

| Model Metric | Model Result |
| ------------ | ------------ |
| Accuracy     | 79.9%        |
| Loss         | 44.3%        |

#### Results - Testing Data

| Model Metric | Model Result |
| ------------ | ------------ |
| Accuracy     | 74.7%        |
| Loss         | 52.1%        |

### Loan Repayment Predictions

The model had an overall accuracy of 75%. The model predicted the class 'student will not repay their loan' slightly higher recall and precision.

## Conclusion

**Data Preparation** : Successfully preprocessed the data for training our neural network model.

**Model Training**: Built and trained a deep learning model on a dataset to predict student loan repayment based on `credit_ranking`.

**Model Evaluation**: Achieved promising results in terms of accuracy and loss.

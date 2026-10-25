# Credit Risk Prediction Using Deep Learning

## Project Overview

This academic project focuses on predicting credit default risk using Multilayer Perceptron (MLP) neural networks.

The objective is to develop, train and evaluate deep learning models capable of classifying potential payment defaults based on financial data.

**Field:** Finance, Risk Management and Deep Learning.

## Dataset

The project uses three datasets:

- Training set: 2,100 observations
- Validation set: 450 observations
- Test set: 450 observations

Each dataset contains four input features and one target variable, `defaut_paiement`, representing whether a payment default occurs.

The CSV files are not included in this repository. They are required to reproduce the experiments.

## Methodology

**1. Data Preparation**
- Import and explore CSV datasets using Pandas.
- Examine data dimensions and missing values.
- Separate explanatory variables from the target variable.

**2. Neural Network Development**
- Build MLP architectures using Keras with the PyTorch backend.
- Use ReLU activation in hidden layers and Sigmoid activation in the output layer.
- Compile models using Adam optimizer and Binary Cross-Entropy loss.

**3. Model Training**
- Train models for 30 epochs with a batch size of 32.
- Monitor training and validation accuracy and loss.
- Compare different neural network architectures.

**4. Model Evaluation**
- Calculate Accuracy, Precision, Recall and F1-score.
- Analyze the confusion matrix and ROC-AUC.
- Examine the impact of classification thresholds.

## Neural Network Architectures

| Model | Architecture | Validation Accuracy |
|---|---|---|
| MLP 1 | 4 → 8 → 1 | 85.33% |
| MLP 2 | 4 → 16 → 1 | 85.78% |
| MLP 3 | 4 → 16 → 8 → 1 | 85.11% |

## Results

The best architecture according to validation accuracy was **MLP 2**, with 16 neurons in one hidden layer.

- Validation Accuracy: **85.78%**
- Test Accuracy: **87.33%**

A separate evaluation of the initial MLP (4 → 16 → 8 → 1) reported:

- Test Accuracy: **87.56%**
- ROC-AUC: **0.8420**
- Recall for default cases: **34.78%**

These results illustrate the importance of evaluating Recall and not relying only on Accuracy, especially with imbalanced classes.

The reported values correspond to the experiments saved in the notebook and may vary when models are retrained.

## Technologies Used

- Python
- Keras
- PyTorch
- Pandas and NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Project Files

- `main.ipynb`: Data exploration, MLP development, training, model comparison and evaluation.

To reproduce the experiments, place `credit_train.csv`, `credit_val.csv` and `credit_test.csv` alongside the notebook and install the required Python libraries.

## Key Learnings

This project helped strengthen practical skills in:

- Deep Learning for financial risk analysis.
- Neural network architecture design.
- Model performance evaluation.
- Credit risk classification.
- Interpretation of classification errors.

## Academic Context

**Master's Program:** Finance, Actuarial Science and Data Science

**Institution:** Abdelmalek Essaâdi University — Faculty of Economics and Management, Tetouan, Morocco.

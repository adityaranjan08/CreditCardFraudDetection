

# Credit Card Fraud Detection

This project aims to develop and evaluate machine learning models to detect fraudulent credit card transactions. The dataset used is highly imbalanced, with the positive class (frauds) accounting for only 0.172% of all transactions.

## Table of Contents
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Models and Evaluation](#models-and-evaluation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Dataset
The dataset used in this project is from Kaggle and contains transactions made by European cardholders in September 2013. It includes:
- 284,807 transactions
- 492 frauds (0.172% of all transactions)

Each transaction has 30 features:
- `Time`: Number of seconds elapsed between this transaction and the first transaction in the dataset
- `V1` to `V28`: Result of a PCA transformation to protect user identities and sensitive features
- `Amount`: Transaction amount
- `Class`: Label (1 for fraud, 0 for non-fraud)

## Project Structure
```
CreditCardFraudDetection/
│
├── data/
│   ├── creditcard.csv
│
├── notebooks/
│   ├── data_exploration.ipynb
│   ├── model_training.ipynb
│
├── src/
│   ├── data_preprocessing.py
│   ├── model.py
│   ├── evaluation.py
│
├── README.md
├── requirements.txt
├── setup.py
└── .gitignore
```

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/adityaranjan08/CreditCardFraudDetection.git
   cd CreditCardFraudDetection
   ```
2. Create a virtual environment and activate it:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. **Data Exploration**: Explore the dataset using the Jupyter notebook `notebooks/data_exploration.ipynb`.
2. **Model Training**: Train and evaluate models using the `notebooks/model_training.ipynb`.
3. **Preprocessing and Model Training**:
   ```bash
   python src/data_preprocessing.py
   python src/model.py
   ```

## Models and Evaluation
We used several machine learning models to detect fraud:
- Logistic Regression
- Decision Tree
- Random Forest
- K-Nearest Neighbors
- Support Vector Machine
- Neural Networks

We evaluated the models using:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

## Results
The best performing model was [KNeighborsClassifier], which achieved the following metrics on the test set:
- Accuracy: 94.46925998874508
- Precision: 89.13372256612267
- Recall: 99.78147885660287
- F1-Score: 94.15753297417795
- ROC-AUC: 94.98147228281107



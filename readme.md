# Heart Disease Prediction using Machine Learning

A Machine Learning project that predicts the probability of heart disease using patient health data. This project demonstrates a complete ML pipeline, including data preprocessing, feature engineering, model training, prediction generation, and submission file creation using a **Random Forest Classifier**.

---

## Project Overview

The objective of this project is to build a machine learning model capable of predicting whether a patient is likely to have heart disease based on various medical attributes.

The workflow includes:

- Data preprocessing
- Missing value handling
- Feature scaling
- Model training
- Model evaluation
- Prediction generation
- Kaggle submission file creation

---

## Project Structure

```
Heart-Disease-Prediction/
│
├── predicting-heart-disease.ipynb    # Main Jupyter Notebook
├── train.csv                         # Training dataset
├── test.csv                          # Testing dataset
├── my_submission.csv                 # Prediction output
├── requirements.txt                  # Project dependencies
└── README.md                         # Project documentation
```

---

## Features

- Load and preprocess datasets
- Handle missing values
- Scale numerical features
- Train a Random Forest model
- Predict heart disease probabilities
- Generate Kaggle-compatible submission file

---

## Technologies Used

- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook

---

## Machine Learning Workflow

### 1. Import Libraries

The project uses:

- Pandas
- NumPy
- Scikit-learn

---

### 2. Load Data

```python
train = pd.read_csv("train.csv")
test = pd.read_csv("test.csv")
```

---

### 3. Data Preprocessing

- Remove unnecessary columns
- Handle missing values
- Separate features and target variable

---

### 4. Feature Scaling

Standardize numerical features using:

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
```

---

### 5. Model Training

The model is trained using a Random Forest Classifier.

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(
    n_estimators=100,
    random_state=42
)
```

---

### 6. Prediction

Generate prediction probabilities:

```python
predictions = model.predict_proba(X_test_scaled)[:, 1]
```

---

### 7. Save Submission

```python
submission.to_csv("my_submission.csv", index=False)
```

---

## 📈 Model

**Random Forest Classifier**

### Advantages

- Handles nonlinear relationships
- Robust against overfitting
- Performs well on structured datasets
- Generates probability predictions
- Requires minimal feature engineering

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/heart-disease-prediction.git
```

Move into the project directory:

```bash
cd heart-disease-prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install pandas numpy scikit-learn jupyter
```

---

## ▶️ Running the Project

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
predicting-heart-disease.ipynb
```

Run all notebook cells from top to bottom.

---

## 📥 Input Files

| File | Description |
|------|-------------|
| train.csv | Training dataset |
| test.csv | Testing dataset |

---

## 📤 Output

After execution, the notebook generates:

```
my_submission.csv
```

Example:

| id | Heart Disease |
|----|----------------|
| 1 | 0.854 |
| 2 | 0.113 |
| 3 | 0.621 |

---

## 📌 Future Improvements

- Hyperparameter tuning
- Cross-validation
- Feature importance visualization
- XGBoost implementation
- LightGBM implementation
- CatBoost implementation
- Ensemble learning
- Confusion Matrix
- ROC Curve
- Precision-Recall Curve
- SHAP Explainability
- Automated feature selection

---

## ⭐ Support

If you found this project helpful, please consider giving it a ⭐ on GitHub. It helps others discover the project and supports future improvements.

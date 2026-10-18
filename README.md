# 🧠 ANN Prediction Model with Churn Modelling Dataset - Deep Learning

[Python](https://img.shields.io/badge/Python-3.8%2B-blue)
[Deep Learning](https://img.shields.io/badge/Deep%20Learning-ANN-red)
[Framework](https://img.shields.io/badge/Framework-TensorFlow%20%7C%20Keras-orange)
[Accuracy](https://img.shields.io/badge/Accuracy-85%25%2B-success)

An end-to-end **Deep Learning** project that predicts customer churn (whether a bank customer will leave or not) using an **Artificial Neural Network (ANN)** on the famous Churn Modelling Dataset.

> Live Notebook: [ANN_MODEL.ipynb](https://github.com/munawirmt/ANN-PREDICTION-MODEL/blob/main/ANN_MODEL.ipynb)

---

### 📌 Problem Statement

In the banking sector, acquiring a new customer is 5x more expensive than retaining one. This model answers a critical business question:
**"Will this customer leave the bank?"**

This is a **Binary Classification** problem solved using Deep Learning.

### 📊 Dataset - Churn_Modelling.csv

Source: Bank Customer Data (10,000 customers)
- **10000 Rows, 14 Columns**
- **Features:**
    - `CreditScore`, `Geography`, `Gender`, `Age`, `Tenure`, `Balance`, `NumOfProducts`, `HasCrCard`, `IsActiveMember`, `EstimatedSalary`
- **Target:**
    - `Exited` - 1 = Customer Left, 0 = Customer Stayed

### 🏗️ ANN Architecture

Built using **TensorFlow & Keras**

Model: Sequential
- Input Layer: 11 neurons (after One-Hot Encoding)
- Hidden Layer 1: 64 neurons, ReLU activation, Dropout 0.2
- Hidden Layer 2: 32 neurons, ReLU activation, Dropout 0.2
- Output Layer: 1 neuron, Sigmoid activation (for Binary Classification)

Optimizer: Adam
Loss Function: Binary Crossentropy
Metrics: Accuracy
Epochs: 100 with EarlyStopping

**Why this architecture?**
- ReLU avoids vanishing gradient problem
- Dropout prevents overfitting
- Sigmoid gives probability between 0 and 1 for Churn
- EarlyStopping prevents wasting epochs

### ⚙️ End-to-End Pipeline

**Step 1: Data Preprocessing**
- Label Encoding for Gender
- One-Hot Encoding for Geography
- Train-Test Split (80-20)

**Step 2: Feature Scaling**
- StandardScaler - Very Important for ANN to converge faster

**Step 3: Build ANN**
- Sequential model with 2 hidden layers

**Step 4: Training & Validation**
- Trained with batch_size=32
- Validation Split to monitor overfitting

**Step 5: Evaluation**
- Confusion Matrix
- Accuracy Score
- Precision, Recall, F1-Score
- ROC-AUC Curve

### 📈 Results

- **Accuracy:** ~85-86%
- **Achieved low loss and high validation accuracy with EarlyStopping**
- Model correctly identifies customers who are likely to churn, helping the bank to take retention actions.

### 📁 Project Structure
ANN-PREDICTION-MODEL/
├── ANN_MODEL.ipynb       # Main Deep Learning Model
├── Churn_Modelling.csv   # Dataset
└── http://README.md


### 🚀 How to Run

1. Clone the repo:
   `git clone https://github.com/munawirmt/ANN-PREDICTION-MODEL.git`
2. Install dependencies:
   `pip install tensorflow scikit-learn pandas matplotlib seaborn`
3. Open `ANN_MODEL.ipynb` in Google Colab / Jupyter
4. Run all cells - Model will train and evaluate automatically

### 💡 Key Learnings

- Why Feature Scaling is mandatory for Neural Networks
- How to handle categorical data with OneHotEncoder & LabelEncoder
- Building a Deep Neural Network from scratch using Keras
- Overfitting control using Dropout & EarlyStopping
- Real-world business impact of Churn Prediction

### 🔮 Future Improvements

- [ ] Build a Streamlit Web App for real-time prediction
- [ ] Try Hyperparameter Tuning with KerasTuner
- [ ] Compare with XGBoost & RandomForest
- [ ] Deploy model using Flask API

### 👨‍💻 Author

**Muhammed Munawir M T**
Aspiring Data Scientist | Deep Learning Enthusiast

- GitHub: [@munawirmt](https://github.com/munawirmt)
- LinkedIn: [Muhammed Munawir M T](https://www.linkedin.com/in/muhammed-munawir-m-t-45b31a286/)

---
⭐ If you like this project, please give it a Star!

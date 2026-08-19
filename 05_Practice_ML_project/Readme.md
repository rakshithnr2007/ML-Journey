# 📈 Practice ML Model

### Basic Market Direction Classifier

A beginner-level Machine Learning project built to understand the **complete ML model-building workflow** through a simple classification problem.

The goal of this project is not to build a real trading system, but to understand how raw data moves through an ML pipeline — from preprocessing and feature selection to training, prediction, and evaluation.

> **Learning project — the dataset is synthetic and is not intended for real-world financial or trading decisions.**

---

## 🎯 Objective

Build a simple classification model that predicts whether the market direction is:

* `0` → DOWN
* `1` → UP

based on two input features:

```text
Market Sentiment + Price Change %
              ↓
       Classification Model
              ↓
       Market Direction
```

---

## 📊 Dataset

The project uses a simple **demo/synthetic dataset** created for practicing the ML workflow.

| Column             | Role        | Description                                     |
| ------------------ | ----------- | ----------------------------------------------- |
| `market_sentiment` | Input       | Market sentiment value                          |
| `price_change_pct` | Input       | Recent percentage change in price               |
| `price_direction`  | Output      | `0 = DOWN`, `1 = UP`                            |
| `unnamed`          | Unnecessary | Extra column used to practice feature selection |

### Input and Output

```python
X = df[['market_sentiment', 'price_change_pct']]
y = df['price_direction']
```

---

## 🔄 Workflow

The notebook (Price_direction_classifier.ipynb) follows the standard ML pipeline:

Data Preprocessing – load trading_classification.csv, drop the unnecessary unnamed column, check for missing values
EDA (Exploratory Data Analysis) – scatter plot of market_sentiment vs price_change_pct, colored by class, to visually confirm the classes are separable
Feature Selection – not required here since only two independent variables are used
Extracting Inputs & Outputs – x = market_sentiment, price_change_pct; y = price_direction
Train-Test Split – 90% train / 10% test using train_test_split()
Feature Scaling – standardizing x_train and x_test using StandardScaler
Model Training – fitting a LogisticRegression model on the training data
Model Evaluation – predicting on the test set and measuring performance with accuracy_score
Decision Boundary Visualization – using mlxtend.plotting.plot_decision_regions to visualize how the model separates the two classes
Deployment – exporting the trained model as model.pkl using pickle, ready to be integrated into a front end / API
---

## 🤖 Machine Learning Model

### Logistic Regression

**Logistic Regression** is used as the classification algorithm.

The model learns patterns from the training data and classifies observations into one of two classes:

```text
0 → DOWN
1 → UP
```

---

## 🧠 Concepts Practiced

* Data loading with Pandas
* Basic EDA
* Feature selection
* Removing unnecessary columns
* Separating `X` and `y`
* Train-test splitting
* Feature scaling with `StandardScaler`
* Logistic Regression
* Model training with `.fit()`
* Prediction with `.predict()`
* Basic model evaluation
* Understanding `y_test` vs `y_pred`
* Decision boundary visualization

---

## 🛠️ Tech Stack

* **Python**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Scikit-learn**
* **Mlxtend**
* **Jupyter Notebook**

---

## 📁 Project Structure

```text
Practice-ML-Model/
│
├── dataset/
│   └── trading_classification.csv
│
├── notebook/
│   └── market_direction_classifier.ipynb
│
└── README.md
```

---

## 📌 Key Takeaway

This project was created to understand the **basic workflow of Machine Learning before going deeper into individual algorithms**.

The main learning progression is:

```text
Understand the workflow
        ↓
Build a simple model
        ↓
Understand what the model is doing
        ↓
Evaluate the model
        ↓
Move to deeper ML concepts
```

---

## 🚀 Next Steps

This project provides the foundation for moving into:

* More classification algorithms
* Regression
* Better model evaluation
* Feature engineering
* Real-world datasets
* Model selection
* More advanced Machine Learning projects

> **Build simple → understand the workflow → go deeper.**


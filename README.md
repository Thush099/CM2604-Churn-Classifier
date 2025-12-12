# CM2604-Churn-Classifier
# CM2604 – Churn Classifier

This project was developed as part of the **CM2604 Machine Learning** module.  
The aim of the project is to build and evaluate machine learning models to predict **customer churn** using the Telco Customer Churn dataset.

---

## Project Overview

Customer churn prediction is an important real-world classification problem where the goal is to identify customers who are likely to leave a service.  
In this project, exploratory data analysis, preprocessing, model training, evaluation, and ethical considerations were carried out following standard machine learning practices taught in the module.

Two models were implemented and compared:
- **Decision Tree Classifier**
- **Neural Network (Multi-Layer Perceptron)**

---

## Dataset

- **Dataset:** Telco Customer Churn  
- **Source:** IBM Sample Dataset  
- **Target variable:** `Churn`  
  - `0` → Customer did not churn  
  - `1` → Customer churned  

The dataset contains customer demographics, service usage details, and billing information.

---

## Exploratory Data Analysis (EDA)

The following analyses were performed:
- Churn class distribution
- Boxplots comparing churn vs non-churn customers for:
  - Tenure
  - Monthly Charges
  - Total Charges
- Categorical feature comparisons (e.g. Contract type, Internet Service)

These plots helped identify patterns and relationships between customer behaviour and churn.

---

## Data Preprocessing

The preprocessing steps include:
- Conversion of `TotalCharges` from text to numeric
- Removal of the identifier column (`customerID`)
- Encoding of categorical variables using **One-Hot Encoding**
- Feature scaling using **StandardScaler**
- Stratified train/test split (80/20)

---

## Handling Class Imbalance

The dataset is imbalanced, with fewer churned customers than non-churned customers.  
To address this:

- **SMOTE (Synthetic Minority Over-sampling Technique)** was applied
- SMOTE was used **only on the training data** to avoid data leakage
- This helps the models learn patterns from the minority class more effectively

---

## Model Development

### Decision Tree
- A baseline Decision Tree model was trained
- Hyperparameter tuning was performed using **GridSearchCV**
- The tree structure was visualised (top 3 levels) for interpretability

### Neural Network
- A simple Multi-Layer Perceptron (MLP) was implemented using Keras
- Dropout was used to reduce overfitting
- Early stopping was applied during training
- Class weights were used to further address class imbalance

---

## Evaluation Metrics

Models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrices
- ROC curves
- Train vs test accuracy comparison
- Generalisation gap analysis

These metrics allow a fair comparison between the Decision Tree and Neural Network models.

---

## Ethical Considerations

Ethical aspects considered in this project include:
- Bias caused by class imbalance
- Responsible use of customer data
- Avoidance of data leakage
- The need for fairness and transparency in churn prediction systems
- Monitoring model performance after deployment

---

## Repository Contents

- `CM2604_Telco_Churn_Project.ipynb` – Full implementation notebook  
- `README.md` – Project overview and documentation  

All code is provided as text in accordance with the coursework requirements.

---

## Author

**Thushanth Mahendran**  
CM2604 – Machine Learning

---

## Notes

This project was developed for academic purposes and follows the methods and techniques taught during the CM2604 module.


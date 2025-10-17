# Decision Tree Diabetes Prediction

This repository contains an implementation of a **Decision Tree Classifier** to predict diabetes likelihood based on diagnostic features such as glucose level, blood pressure, insulin level, and BMI.  
The project was developed as part of the **CSC 361 – Artificial Intelligence** course at **King Saud University**.

---

##  Project Overview
The main goal of this project is to build and evaluate a Decision Tree model that classifies patients as either **diabetic** or **non-diabetic** based on medical data.

###  Dataset
The dataset includes 768 instances and 8 medical attributes:
- Pregnancies  
- Glucose  
- Blood Pressure  
- Skin Thickness  
- Insulin  
- BMI  
- Diabetes Pedigree Function  
- Age  

> [🔗 Dataset Link (Google Sheets)](https://docs.google.com/spreadsheets/d/13LjNK_qGKSybKZH48AlsT4fQGxRDjVNRXP47scQ8wpY/edit)

---

##  Tools and Libraries
- **Python**
- **Google Colab**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**

---

##  Implementation Steps
1. **Data Preprocessing**  
   - Replaced zero values in invalid medical fields (e.g., insulin, skin thickness).  
   - Applied normalization for numerical features to improve model accuracy.  

2. **Model Building**  
   - Algorithm: `DecisionTreeClassifier` from Scikit-learn.  
   - Split ratio: 70% training / 30% testing.  
   - Two configurations were tested:
     - Gini Index (Max Depth = 3)  
     - Entropy (Max Depth = 5)

---

## Experimental Results
| Configuration | Criterion | Max Depth | Accuracy | Notes |
|----------------|------------|------------|-----------|--------|
| 1 | Gini Index | 3 | 65.22% | Baseline model |
| 2 | Entropy | 5 | 76.09% | Improved after normalization |


### Confusion Matrix (Normalized Data)

| Actual \ Predicted | 0 (Non-Diabetic) | 1 (Diabetic) |
|--------------------|------------------|---------------|
| **0 (Non-Diabetic)** | 140 | 10 |
| **1 (Diabetic)** | 45 | 35 |


- The normalization improved the accuracy from **65.22% → 76.09%**.

---

## Discussion
The Decision Tree model successfully distinguished between diabetic and non-diabetic cases.  
However, further optimization (e.g., hyperparameter tuning, pruning) could enhance generalization and reduce overfitting.

---

## Colab Notebook
Open and run the notebook in Google Colab:  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1HZ11-rvk--XVf5GabOcWw6B1l_r61xeg?usp=sharing)





 

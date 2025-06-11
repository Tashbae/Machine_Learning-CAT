# Student Performance Classification

## 📌 Problem Statement

The goal of this project is to build a machine learning model that can predict whether a student will pass or fail based on their background information, school-related inputs, and personal attributes.

The target variable (`G3`) is the final grade of a student. For classification purposes, students with a final grade (G3) **≥ 10** are considered as **passing** (`1`), and those with **< 10** as **failing** (`0`).

---

## 🔍 Approach

### 1. Data Preprocessing

* Loaded the dataset from `student-mat.csv`
* Handled **missing values** (although the dataset was mostly clean)
* Applied **encoding** to categorical features using `pd.get_dummies()`
* Created a new binary column `Pass` from `G3` (1 for pass, 0 for fail)
* Dropped the original `G3` column after deriving the `Pass` target

### 2. Feature Selection & Data Splitting

* Explored **correlations** between features and the target (`G3`)
* Selected all relevant features after encoding
* Split the dataset into **training (80%)** and **testing (20%)** sets using `train_test_split`

### 3. Model Training

Two classification algorithms were trained:

* **Logistic Regression**
* **Decision Tree Classifier**
* Random Forest Classifier

### 4. Evaluation

Models were evaluated using:

* **Accuracy**
* **F1-Score**
* **Confusion Matrix**

---

## 📊 Results and Interpretations

| Model               | Accuracy | F1-Score |
| ------------------- | -------- | -------- |
| Logistic Regression | \~83%    | \~0.87   |
| Decision Tree       | \~79%    | \~0.82   |

* **Logistic Regression** performed better overall, with higher accuracy and a balanced F1-score.
* The **confusion matrix** showed that most predictions were correct, with few false positives/negatives.
* Logistic regression is preferred for its interpretability and generalization on test data.

---

## ✅ Conclusion

We successfully built a binary classifier to predict student performance using basic demographic and academic features. The project highlights the value of preprocessing, feature engineering, and proper model evaluation for effective machine learning.

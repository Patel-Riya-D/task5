# task5
# 🩺 Heart Disease Prediction - Decision Trees & Random Forests

## 📌 Objective
The goal of this task is to learn and apply tree-based classification models — specifically **Decision Trees** and **Random Forests** — to predict the presence of heart disease based on medical attributes.

---

## 📊 Dataset
- **File**: `heart.csv`
- **Target**: `target` column (0 = No Disease, 1 = Disease)
- Contains patient medical data like age, sex, chest pain type, cholesterol, max heart rate, etc.

---

## 🧠 Models Used
- `DecisionTreeClassifier` from Scikit-learn
- `RandomForestClassifier` from Scikit-learn

---

## 🔍 Steps Performed

### ✅ Data Preprocessing
- Checked for nulls and data types
- Verified class balance
- Split dataset into training and testing sets (80/20)

### 🌳 Decision Tree
- Trained a basic decision tree
- Visualized the full tree
- Evaluated using precision, recall, F1-score

### 🌲 Random Forest
- Trained with 100 estimators
- Evaluated performance
- Extracted feature importances

### ⚖️ Overfitting Analysis
- Varied tree depth from 1 to 20
- Plotted training vs testing accuracy
- Identified depth 9–10 as optimal

### 🔁 Cross-Validation
- 5-fold cross-validation applied to both models

---

## 📈 Results

### ✅ **Classification Reports**

| Model            | Accuracy | Precision (1) | Recall (1) | F1-Score (1) |
|------------------|----------|----------------|-------------|---------------|
| Decision Tree    | 99%      | 1.00           | 0.97        | 0.99          |
| Random Forest    | 99%      | 1.00           | 0.97        | 0.99          |

### 🔁 **Cross-Validation Scores**

- **Decision Tree**: `1.0000`
- **Random Forest**: `0.9971`

---

## 📊 Visualizations

### 1. Overfitting Analysis
![Overfitting Analysis](overfitting_plot.png)

- Training accuracy reaches 100% at depth > 10
- Test accuracy plateaus at ~98% around depth 9–10
- Helps determine optimal pruning level

---

### 2. Decision Tree Structure
![Decision Tree](decision_tree.png)

- Shows how splits are made on features like `ca`, `thal`, `cp`
- Color-coded nodes indicate predicted class

---

### 3. Random Forest Feature Importances
![Feature Importances](feature_importance.png)

- Most important features:
  - `cp` (chest pain)
  - `ca` (major vessels)
  - `thalach` (max heart rate)
  - `oldpeak` (ST depression)

---

## 📌 Conclusion
- Both models achieved high accuracy (~99%) on this dataset.
- **Random Forest** generalizes slightly better and ranks features by importance.
- **Decision Tree** is highly interpretable but may overfit on deep levels.
- Feature importance analysis shows `cp`, `ca`, and `thalach` are key indicators for heart disease.

---

## 💾 Files Included
- `heart.csv` — dataset used
- `task5.ipynb` — full code notebook
- `overfitting_plot.png` — training vs testing accuracy
- `decision_tree.png` — tree visualization
- `feature_importance.png` — RF feature importance
- `README.md` — this summary

---


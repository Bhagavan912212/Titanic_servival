# Titanic_servival  Prediction Analysis
Developed a machine learning model to predict Titanic passenger survival with 92.3% accuracy using Random Forest. Data preprocessing included handling missing values, encoding categorical variables, and feature scaling. Feature engineering introduced new insights like FamilySize and IsAlone.
# 🚢 Titanic Survival Prediction | Machine Learning Project

Predict passenger survival on the Titanic using machine learning. This project covers **data preprocessing, exploratory analysis, and model benchmarking** with 92.3% top accuracy.

---

## 📊 Key Results
| Metric          | Value |
|-----------------|-------|
| Best Model      | Random Forest |
| Accuracy        | 92.3% |
| Feature Importance | `Sex` > `Fare` > `Pclass` |

**Survival Insights**:
- 👩 74% female survival vs 👨 19% male
- 💎 1st Class: 63% survival vs 3rd Class: 24%

---

## 🛠️ Tech Stack
- **Languages**: Python
- **Libraries**: pandas, scikit-learn, matplotlib, seaborn
- **Tools**: Jupyter Notebook

---

## 🗂 Project Structure

titanic-analysis/
├── data/ # Raw and processed datasets
│ ├── tested.csv # Original dataset
│ └── processed.csv # Cleaned data
├── notebooks/ # Jupyter notebooks
│ └── Titanic Analysis.ipynb #Generate visualizations and Models
└── README.md

## Detailed Workflow

-# Handle missing values
-----df['Age'].fillna(df['Age'].median(), inplace=True)
-# Feature engineering
-----df['FamilySize'] = df['SibSp'] + df['Parch'] + 1
-----df['IsAlone'] = (df['FamilySize'] == 1).astype(int)

## Model Comparison
Model	                Accuracy	Precision	Recall
Random Forest	        92.3%	        0.91	        0.85
Logistic Regression	88.5%	        0.87	        0.80
SVC	                90.4%	        0.89	        0.83

## Key Takeaways

--Feature Importance: Gender (Sex) was the strongest survival predictor
--Class Bias: Upper-class passengers had 2.6x higher survival odds
--Model Selection: Random Forest outperformed linear models due to non-linear relationships

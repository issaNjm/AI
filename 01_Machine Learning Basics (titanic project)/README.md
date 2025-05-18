# Titanic Survival Prediction Project — Summary

## 1. Data Visualization (Exploratory Data Analysis)

- Loaded the Titanic dataset and explored basic statistics and missing values.
- Visualized the distribution of the target variable (Survived) to check for class imbalance.
- Analyzed survival rates across key features like gender (`Sex`), passenger class (`Pclass`), and age groups (`AgeGroup`).
- Created age bins to categorize passengers into meaningful groups (Child, Teen, Adult, etc.).
- Used plots (countplots, bar charts) to understand relationships between features and survival.

## 2. Data Preprocessing

- Handled missing values by filling numerical features (`Age`, `Fare`) with median values and categorical features (`Embarked`) with mode.
- Extracted new features such as Title from passenger names and simplified rare titles.
- Encoded categorical variables:
  - Label encoded binary variables like `Sex`.
  - One-hot encoded multi-class variables such as `Embarked`, `Title`, and `AgeGroup`.
- Normalized continuous features (`Fare`) using Min-Max scaling.
- Dropped irrelevant or unique identifier columns like `PassengerId`, `Ticket`, and `Name` for model training.
- Ensured consistent preprocessing of training and test datasets, including matching one-hot encoded columns.

## 3. Model Creation and Evaluation

- Built multiple classification models including Logistic Regression, Random Forest, and XGBoost.
- Used cross-validation (`StratifiedKFold`) to evaluate model robustness and avoid overfitting.
- Calculated performance metrics including accuracy, precision, recall, and confusion matrices.
- Stored evaluation results for each model for comparison.

## 4. Hyperparameter Tuning

- Applied `GridSearchCV` to perform exhaustive hyperparameter tuning for each model.
- Defined parameter grids for Logistic Regression, Random Forest, and XGBoost.
- Identified best hyperparameters based on cross-validation accuracy.
- Evaluated tuned models on the test dataset and compared metrics.
- Selected the best performing model based on the chosen metric (e.g., accuracy).

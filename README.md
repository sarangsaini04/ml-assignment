

## a. Problem Statement
The objective of this project is to build and evaluate machine learning classification models that predict whether an individual's annual income exceeds $50,000 per year based on demographic, educational, and occupational information from the Adult Census Income Dataset. The dataset contains 48,842 records with 14 features, including age, education, occupation, marital status, work hours, and other census-related attributes.

This is a binary classification problem, where the target variable has two classes:
<=50K: Annual income is less than or equal to $50,000.
>50K: Annual income is greater than $50,000.

Accurately predicting income categories is valuable for socioeconomic research, policy planning, workforce analysis, and targeted decision-making. By comparing multiple machine learning algorithms such as Logistic Regression, Decision Tree, K-Nearest Neighbors (KNN), Naive Bayes, and Support Vector Machine (SVM), this project identifies the model that provides the most reliable predictions for income classification while analyzing key performance metrics such as Accuracy, Precision, Recall, F1-Score, MCC, and AUC.

This study demonstrates how machine learning can leverage census data to uncover patterns associated with income levels and support data-driven decision-making in social and economic domains

## b. Dataset Description
- Source: https://archive.ics.uci.edu/dataset/2/adult
- Instances: 48,842 | Features: 14 | Target: income (2 classes: <=50K, >50K) 【1-8675e1】
- Feature types:
  - Numerical (6): age, fnlwgt, education-num, capital-gain, capital-loss, hours-per-week
  - Categorical/Binary (8): workclass, education, marital-status, occupation, relationship, race, sex, native-country 【1-8675e1】
- Class distribution:
  - <=50K: Majority class
  - >50K: Minority class (income prediction dataset) 【1-8675e1】
- Missing values:
  - Present in workclass, occupation, and native-country attributes. 【1-8675e1】
- Preprocessing:
  - Missing values handled (removed or imputed)
  - Categorical features encoded (e.g., One-Hot Encoding)
  - Numerical features scaled/standardized
  - Dataset split into 80% training and 20% testing using stratified sampling (random_state=42)

## c. GitHub Repository Link
https://github.com/sarangsaini04/ml-assignment.git

## d. Models Used

### Comparison Table
| ML Model Name          |   Accuracy |    AUC |   Precision |   Recall |     F1 |    MCC |
|:-----------------------|-----------:|-------:|------------:|---------:|-------:|-------:|
| Logistic Regression    |     0.856  | 0.9098 |      0.7397 |   0.6199 | 0.6745 | 0.5867 |
| Decision Tree          |     0.815  | 0.7547 |      0.6107 |   0.6384 | 0.6243 | 0.5018 |
| KNN                    |     0.8365 | 0.868  |      0.6745 |   0.6199 | 0.6461 | 0.5408 |
| Naive Bayes            |     0.5421 | 0.7498 |      0.3395 |   0.9541 | 0.5008 | 0.3341 |
| Support Vector Machine |     0.8601 | 0.9066 |      0.7673 |   0.6014 | 0.6743 | 0.594  |

### Observations

| ML Model Name | Observation about model performance |
|:----------------------|:--------------------------------------------------------------|
| Logistic Regression | Strong baseline model with the highest AUC (0.9098) and F1-score (0.6745), showing balanced classification performance and good class separability. |
| Decision Tree | Lowest performance among major models, with lower Accuracy, AUC, F1-score, and MCC, indicating weaker generalization and possible overfitting. |
| KNN | Moderate performance with reasonable Accuracy (0.8365) and AUC (0.8680), but lower Precision and MCC than Logistic Regression and SVM. |
| Naive Bayes | Achieves the highest Recall (0.9541), capturing most positive instances, but suffers from very low Precision and Accuracy due to many false positives. |
| Support Vector Machine | Best overall performer with the highest Accuracy (0.8601), Precision (0.7673), and MCC (0.5940), demonstrating strong and balanced classification performance. |

**Overall winner for this dataset:** Support Vector Machine (SVM), because it achieved the highest Accuracy (0.8601), Precision (0.7673), and MCC (0.5940) while maintaining a high AUC (0.9066) and competitive F1-score (0.6743). These metrics indicate the most balanced and reliable performance across classes.

## Live App
https://ml-assignment-gbn2m6qlhdg6xxge7hyvlb.streamlit.app/

## How to run locally
pip install -r requirements.txt
python train_models.py
streamlit run app.py









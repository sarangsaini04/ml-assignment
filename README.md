# <Your Project Title>

## a. Problem Statement
The objective of this project is to build and evaluate machine learning classification models that predict whether an individual's annual income exceeds $50,000 per year based on demographic, educational, and occupational information from the Adult Census Income Dataset. The dataset contains 48,842 records with 14 features, including age, education, occupation, marital status, work hours, and other census-related attributes.

This is a binary classification problem, where the target variable has two classes:

<=50K: Annual income is less than or equal to $50,000.
>50K: Annual income is greater than $50,000.

Accurately predicting income categories is valuable for socioeconomic research, policy planning, workforce analysis, and targeted decision-making. By comparing multiple machine learning algorithms such as Logistic Regression, Decision Tree, K-Nearest Neighbors (KNN), Naive Bayes, and Support Vector Machine (SVM), this project identifies the model that provides the most reliable predictions for income classification while analyzing key performance metrics such as Accuracy, Precision, Recall, F1-Score, MCC, and AUC.

This study demonstrates how machine learning can leverage census data to uncover patterns associated with income levels and support data-driven decision-making in social and economic domains

## b. Dataset Description  [1 mark]
- Source: <UCI/Kaggle link>
- Instances: <N> | Features: <N> | Target: <name> (<classes>)
- Feature types, class distribution, missing values, preprocessing done (scaling, encoding, 80/20 stratified split, random_state=42).

## c. GitHub Repository Link
https://github.com/<username>/<repo>

## d. Models Used  [5 marks]

### Comparison Table
| ML Model Name | Accuracy | AUC | Precision | Recall | F1 | MCC |
|---|---|---|---|---|---|---|
| Logistic Regression | | | | | | |
| Decision Tree | | | | | | |
| KNN | | | | | | |
| Naive Bayes | | | | | | |
| Support Vector Machine | | | | | | |

### Observations  [3 marks]
| ML Model Name | Observation about model performance |
|---|---|
| Logistic Regression | e.g. "Strong baseline, but lower MCC because classes X and Y overlap non-linearly." |
| Decision Tree | ... |
| KNN | ... |
| Naive Bayes | ... (independence assumption, speed) |
| Support Vector Machine | ... |

**Overall winner for this dataset:** <model>, because <reasons based on metrics: MCC, F1, AUC, training time>.

## Live App
https://<your-app>.streamlit.app

## How to run locally
pip install -r requirements.txt
python train_models.py
streamlit run app.py







| ML Model Name          |   Accuracy |    AUC |   Precision |   Recall |     F1 |    MCC |
|:-----------------------|-----------:|-------:|------------:|---------:|-------:|-------:|
| Logistic Regression    |     0.856  | 0.9098 |      0.7397 |   0.6199 | 0.6745 | 0.5867 |
| Decision Tree          |     0.815  | 0.7547 |      0.6107 |   0.6384 | 0.6243 | 0.5018 |
| KNN                    |     0.8365 | 0.868  |      0.6745 |   0.6199 | 0.6461 | 0.5408 |
| Naive Bayes            |     0.5421 | 0.7498 |      0.3395 |   0.9541 | 0.5008 | 0.3341 |
| Support Vector Machine |     0.8601 | 0.9066 |      0.7673 |   0.6014 | 0.6743 | 0.594  |

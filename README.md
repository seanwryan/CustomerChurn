Telco Customer Churn Prediction
Overview
This project aims to predict customer churn for a telecommunications company using machine learning models. By identifying customers likely to churn, the company can take proactive measures to retain them and improve business performance.

Dataset
The dataset used for this project is the "Telco Customer Churn" dataset from Kaggle. It contains 7,043 entries with 21 columns, including customer demographics, account information, and service usage details.

Project Steps
1. Data Exploration and Cleaning
Converted TotalCharges to numeric and handled missing values.
Dropped the customerID column.
Performed one-hot encoding on categorical features.
Created new features: tenure groups and average monthly charges.
2. Feature Selection
Used Recursive Feature Elimination (RFE) with a RandomForestClassifier to select the top 10 significant features:
tenure
MonthlyCharges
TotalCharges
avg_monthly_charges
gender_Male
InternetService_Fiber optic
Contract_One year
Contract_Two year
PaperlessBilling_Yes
PaymentMethod_Electronic check
3. Model Building
Implemented and evaluated Logistic Regression, Random Forest, and Gradient Boosting models.
Performed hyperparameter tuning for Gradient Boosting.
4. Model Improvement
Addressed class imbalance using SMOTE (Synthetic Minority Over-sampling Technique).
Implemented a Stacking Classifier combining Random Forest and Gradient Boosting models with a Logistic Regression meta-model.
Conducted hyperparameter tuning for the Stacking Classifier.
5. SHAP Analysis
Used SHAP (SHapley Additive exPlanations) to analyze feature importance and interpret model predictions.
6. Results
Logistic Regression: Accuracy: 0.79, Precision: 0.62, Recall: 0.52, F1-Score: 0.56
Random Forest: Accuracy: 0.78, Precision: 0.63, Recall: 0.47, F1-Score: 0.54
Gradient Boosting: Accuracy: 0.79, Precision: 0.64, Recall: 0.48, F1-Score: 0.55
Tuned Gradient Boosting: Accuracy: 0.79, Precision: 0.63, Recall: 0.50, F1-Score: 0.56
Tuned GB with SMOTE: Accuracy: 0.77, Precision: 0.56, Recall: 0.65, F1-Score: 0.60
Stacking Classifier: Accuracy: 0.79, Precision: 0.64, Recall: 0.47, F1-Score: 0.54
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/telco-customer-churn-prediction.git
cd telco-customer-churn-prediction
Install required packages:

bash
Copy code
pip install -r requirements.txt
Download the dataset from Kaggle and place it in the project directory:

Telco Customer Churn Dataset
Usage
Run the Jupyter notebook or Python scripts to replicate the analysis and results. Ensure you have the dataset in the correct directory.

Future Work
Further feature engineering and exploration of additional models like XGBoost or LightGBM.
More sophisticated hyperparameter tuning techniques.
Investigating additional techniques for handling class imbalance.
Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or new features.

License
This project is licensed under the MIT License.

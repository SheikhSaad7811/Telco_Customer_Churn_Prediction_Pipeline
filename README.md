# Telco Customer Churn Prediction (End-to-End ML Pipeline)

## 📌 Objective
The goal of this project is to build a **reusable and production-ready machine learning pipeline** for predicting customer churn using the **Telco Customer Churn Dataset**.  
This project demonstrates how to design an end-to-end pipeline that includes **data preprocessing, model training, hyperparameter tuning, evaluation, and export** for deployment.

---

## ⚙️ Methodology / Approach
1. **Dataset**: Telco Customer Churn dataset (`WA_Fn-UseC_-Telco-Customer-Churn.csv`).
2. **Preprocessing**:
   - Removed irrelevant identifiers (`customerID`).
   - Handled missing values in `TotalCharges`.
   - Scaled numerical features using `StandardScaler`.
   - Encoded categorical features using `OneHotEncoder`.
3. **Pipeline Construction**:
   - Used `Pipeline` and `ColumnTransformer` from scikit-learn to combine preprocessing + model.
4. **Models**:
   - Logistic Regression
   - Random Forest
5. **Hyperparameter Tuning**:
   - Used `GridSearchCV` with cross-validation to optimize hyperparameters.
6. **Evaluation Metrics**:
   - Accuracy
   - Classification Report (Precision, Recall, F1-score)
   - Confusion Matrix
   - ROC Curve
   - Feature Importances (for Random Forest)
7. **Export**:
   - Saved the trained pipeline with `joblib` for production reuse.

---

## 📊 Key Results / Observations
- The **best model** was selected automatically using GridSearchCV.  
- Achieved strong performance on the test set with good **accuracy and recall** for churn prediction.  
- **Sample predictions** showed the pipeline can directly predict churn (0 = No, 1 = Yes).  
- Confusion Matrix and ROC Curve provided deeper insights into model performance.  
- For Random Forest, feature importance analysis highlighted which customer attributes most influenced churn.  
- The entire pipeline was exported as `churn_pipeline.joblib`, making it easy to load and use in a production environment.

---

## 🚀 How to Use
1. Upload dataset to Colab or local environment.  
2. Run the notebook to train and evaluate the pipeline.  
3. Load the saved model (`churn_pipeline.joblib`) to make predictions on new customer data.  

---

## 🛠️ Skills Gained
- End-to-end ML pipeline construction with scikit-learn  
- Hyperparameter tuning with GridSearchCV  
- Model evaluation & visualization  
- Exporting and reusing ML pipelines in production  

# 🪙 Credit Score Classification
This project develops **machine learning models** to classify customers into **Poor, Standard, or Good** categories based on their historical financial data. The goal is to identify distinct customer risk profiles to enable data-driven credit decisions and optimize lending strategies.

## ⚙️ Workflow

1. Exploratory Data Analysis
   
   - Identified unique values (such as ID, Customer_ID, Name, and SSN), duplicates, missing values, and inconsistent values.
   - Checked for string/object columns that have to be changed into appropriate numeric types for model compatibility
     
3. Data Preprocessing
   - Removed unique values data
   - Handled inconsistent values on some features (e.g. Occupation, Payment_Behavior, etc)
   - Engineered label into 0 (Poor), 1 (Standard), 2 (Good) and Credit History Age (from years & months into months only)
   - Feature Selection based on correlation shown by heatmap
   - Treated outliers using Winsorization
     
4. Modelling & Evaluation
   - Applied Random Forest Classifier and XGB Classifier to train on the preprocessed predictor features and predict the target variable
   - Compared performance based on evaluation metrics

## 📈 Results and Conclusion
- XGBoost Classifier significantly outperforms the Random Forest Classifier across all evaluation metrics, achieving a higher overall accuracy (75% vs. 66%)
- Utilizing GridSearchCV to optimize hyperparameters proves highly effective in boosting macro-averaged Recall and F1-score.
- XGBoost model provides a balanced and reliable credit classification system, allowing financial institutions to better identify high-risk (Poor) and high-value (Good) customers while minimizing default risks.

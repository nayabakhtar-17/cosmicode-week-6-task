# *REPORT*
# Week 6 Of ML 
# Project.....Predicting Adult Income using Machine Learning

# 📑 Machine Learning Project Report

*Title:* Predicting Adult Income using Machine Learning

## *1. Problem Definition*

The goal of this project is to predict whether an individual’s annual income exceeds **\$50,000** based on demographic and employment-related features such as age, education, occupation, and hours worked per week. This is a **binary classification problem**.

## *2. Dataset Description*

* **Source:** UCI Machine Learning Repository – Adult Income Dataset
* **Size:** 48,842 rows, 15 features
* **Features include:**

  * Age, Education, Workclass, Occupation, Marital Status, Race, Sex
  * Capital Gain, Capital Loss, Hours per Week, Native Country
* **Target Variable:** Income (`>50K` or `<=50K`)

The dataset is suitable for both **traditional ML** and **deep learning models** due to its structured tabular format.

## *3. Data Preprocessing & Exploratory Data Analysis (EDA)*

### Preprocessing Steps:

* Replaced `"?"` values with `NaN` and dropped missing rows.
* Applied **Label Encoding** on categorical features (e.g., workclass, education).
* Normalized numerical features using **StandardScaler**.
* Created a new feature **`capital_total = capital_gain - capital_loss`** for feature engineering.

### EDA Insights:

* **Income Distribution:** Majority of individuals earn <=50K.
* **Age vs Income:** Higher income groups tend to be older on average.
* **Education:** Higher education levels correlate strongly with higher income.
* **Hours per week:** People working more hours generally fall into the >50K category.

## **4. Model Building & Comparison**

We trained and compared multiple models:

| Model                  | Accuracy |
| ---------------------- | -------- |
| Logistic Regression    | \~82%    |
| Decision Tree          | \~81%    |
| K-Nearest Neighbors    | \~79%    |
| Support Vector Machine | \~84%    |
| Random Forest          | \~86%    |
| Deep Learning (MLP)    | \~85%    |

📌 **Random Forest performed the best** among traditional ML models.

## **5. Feature Engineering Impact**

* Adding `capital_total` improved model accuracy by \~1%.
* Encoding categorical variables increased model stability.
* Feature scaling ensured fair weight distribution across features.

## **6. Hyperparameter Tuning & Cross Validation**

We tuned **Random Forest** using GridSearchCV.

* **Best Parameters:**

  * n\_estimators = 200
  * max\_depth = 20
  * min\_samples\_split = 5

* **Cross-validated Accuracy:** \~87%

This tuned Random Forest was chosen as the **final model**.


## *7. Model Deployment*

We deployed the final model using **Flask** inside Google Colab (with `flask-ngrok`).

* A simple **web interface** was created where users can enter:

  * Age
  * Education Number
  * Hours per Week
* The model predicts: **Income >50K or <=50K**.

This deployment demonstrates how a trained ML model can be integrated into a **real-world web application**.

## *8. Conclusion*

* The project successfully applied **data preprocessing, EDA, model building, feature engineering, hyperparameter tuning, and deployment**.
* The best-performing model was **Random Forest (87% accuracy)**.
* The model was deployed using Flask, allowing user interaction via a web interface.
* This end-to-end pipeline demonstrates the full **machine learning project lifecycle** learned during the internship.

## *9. Future Work*

* Deploy model on a cloud service (Heroku, AWS, or Streamlit).
* Use advanced **ensemble methods (XGBoost, LightGBM)** for higher accuracy.
* Build a more interactive web app with additional input fields.

## *10. References*

* UCI Machine Learning Repository: Adult Income Dataset
* Scikit-learn, TensorFlow, Flask Documentation
 
# you can visit my google colab notebook to see all the taska in running form

https://colab.research.google.com/drive/1CkjC9R75Mb2NQdAIytPE8LzNttgUohMF?usp=sharing

# AUTHOR : NAYAB AKHTAR




# 🩺 Cirrhosis Stage Classification in Machine Learning Using Python
This project focuses on building a multi-class classification model to predict the histologic stage of cirrhosis in patients. Developed as part of a Machine Learning course, the goal is to leverage patient data to accurately classify the disease into one of four stages.

The dataset is notably imbalanced, making this a challenging classification task. The project involves a thorough Exploratory Data Analysis (EDA), handling of missing values, and a comparison between two powerful ensemble models: **Random Forest** and **XGBoost**. Additionally, the impact of oversampling with **SMOTE** is investigated to address the class imbalance.

---

### 📊 Dataset Description
The data for this project is the **Cirrhosis Prediction Dataset**, sourced from Kaggle. It contains records for 418 patients with 20 distinct attributes.
* **Source:** **[Cirrhosis Prediction Dataset on Kaggle](https://www.kaggle.com/datasets/fedesoriano/cirrhosis-prediction-dataset)**
* **Features:** The dataset includes a mix of numerical and categorical features like `N_Days` (duration of observation), `Age`, `Sex`, `Drug` administered, and various biochemical markers such as `Bilirubin`, `Cholesterol`, `Albumin`, and `Copper`.
* **Target Variable:** The `Stage` column is the multi-class target, indicating the histologic stage of the disease (1, 2, 3, or 4).

---

### ⚙️ Model Training & Evaluation
Two ensemble models were trained and evaluated: one without oversampling and one with SMOTE-balanced data.
#### 1. Random Forest Classifier
A strong baseline model that is effective with tabular data and less sensitive to scaling.
#### 2. XGBoost Classifier
A powerful gradient boosting algorithm known for its high predictive accuracy, especially in medical datasets. **XGBoost with SMOTE** was chosen as the final and best-performing model due to its ability to better handle the imbalanced classes.
#### Final Model Performance (Oversampled XGBoost)
The classification report for the XGBoost model trained on the SMOTE-balanced data showed:
* **Accuracy:** 58%. While modest, accuracy is not the primary metric for imbalanced datasets.
* **Macro Avg Recall:** 57%. This indicates the model is reasonably effective at identifying patients across all stages.
* **Class Performance:** The model performed best on Stage 4 (recall of 78%), likely because it is a more distinct and severe category. It struggled most with the minority classes (Stage 1 and 2), showing a trade-off between precision and recall.


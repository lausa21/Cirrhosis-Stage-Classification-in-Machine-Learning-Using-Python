# 🩺 Cirrhosis Stage Classification in Machine Learning Using Python
This project focuses on building a **multi-class classification model to predict the histologic stage of cirrhosis in patients**. Developed as part of a Machine Learning course in my 3rd-semester, the goal is to leverage patient data to accurately classify the disease into one of four stages.

The dataset is notably imbalanced, making this a challenging classification task. The project involves a thorough Exploratory Data Analysis (EDA), handling of missing values, and a comparison between two powerful ensemble models: Random Forest and XGBoost. Additionally, the impact of oversampling with SMOTE is investigated to address the class imbalance.

---

### 📊 Dataset Description
* The dataset file is included in this directory. It contains records for 418 patients with 20 distinct attributes.
* **Features:** The dataset includes a mix of numerical and categorical features like `N_Days` (duration of observation), `Age`, `Sex`, `Drug` administered, and various biochemical markers such as `Bilirubin`, `Cholesterol`, `Albumin`, and `Copper`.
* **Target Variable:** The `Stage` column is the multi-class target, indicating the histologic stage of the disease (1, 2, 3, or 4).

---

### ⚙️ Model Training & Evaluation
Two ensemble models (Random Forest Classifier and XGBoost Classifier) were trained and evaluated: one without oversampling and one with SMOTE-balanced data. The **XGBoost Classifier** trained on the oversampled (SMOTE) data was chosen as the final and best-performing model.

#### Final Model Performance (Oversampled XGBoost)
The classification report provides a detailed look at the model's performance:

| Stage | Precision | Recall | F1-Score | Support |
| :--- | :--- | :--- | :--- | :--- |
| **1 (Stage 1)** | 0.40 | 0.33 | 0.36 | 6 |
| **2 (Stage 2)** | 0.19 | 0.22 | 0.21 | 18 |
| **3 (Stage 3)** | 0.52 | 0.54 | 0.53 | 28 |
| **4 (Stage 4)** | 0.64 | 0.58 | 0.61 | 31 |
| **Accuracy** | | | **0.47** | **83** |
| **Macro Avg** | 0.44 | 0.42 | 0.43 | 83 |
| **Weighted Avg** | 0.48 | 0.47 | 0.48 | 83 |

### 🏆 Conclusion
* Random Forest (after resampling and tuning) showed an overall improvement in precision, recall, and F1-score, with a more consistent and balanced performance across all classes.
* Random Forest also has the highest score of F1-score weighted.
* So, Random Forest after resampling and tuning is chosen as best model among others.

---

### 🎯 Top 5 Feature Importances
Below are the top 5 most important features in predicting the stage of cirrhosis using the Random Forest model after oversampling and tuning.
1.  **Prothrombin (13.27%):** Prothrombin is an essential indicator of liver function related to clotting. Low prothrombin levels can indicate severe liver damage, heavily influencing stage prediction.
2.  **Platelets (12.67%):** Platelet count is often used to assess liver disease severity. In cirrhosis, platelet counts tend to be reduced, making it a critical marker for liver health.
3.  **Albumin (12.24%):** Albumin plays a crucial role in predicting cirrhosis stages. Low albumin levels are commonly associated with liver dysfunction and help identify the severity of the condition.
4.  **Age (10.82%):** Age is a significant factor, as the risk of liver disease and its progression often increases with age.
5.  **Bilirubin (10.16%):** Bilirubin levels increase when the liver’s ability to process waste is impaired. High levels are an important marker of liver dysfunction or cirrhosis.

---

### 🛠️ Concepts
* **Language:** Python
* **Core Concepts:**
    * Exploratory Data Analysis (EDA) & Data Pre-Processing
    * Feature Encoding and Scaling
    * Oversampling using SMOTE
    * Model Training (Random Forest & XGBoost)
    * Evaluation (Confusion Matrix, Classification Report)

---

 ### 🖋 Author
Laurel Evelina Widjaja

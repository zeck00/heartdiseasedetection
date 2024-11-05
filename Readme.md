
## **❤️ Heart Disease Dataset Analysis & Model Evaluation 📊**

Dataset source on Kaggle: [Heart Disease Dataset](https://www.kaggle.com/datasets/snmahsa/heart-disease/data)

---

### **📜 Dataset Overview**
The **Heart Disease Dataset** 📂 from Kaggle provides critical insights into factors influencing heart disease risk. This dataset assists healthcare professionals by highlighting various health attributes, making it a valuable resource for:

- **Understanding risk factors** like cholesterol, blood pressure, and heart rate 💓
- **Building predictive models** for diagnostic accuracy and preventive care ⚕️

This well-structured dataset is ideal for creating and testing machine learning models to predict heart disease likelihood. It provides 1,035 entries with 16 features per patient, enabling a comprehensive analysis.

---

### **🔍 Key Features**

Each patient record includes essential attributes:

- **🧑‍⚕️ sex:** Male (1) or Female (0) – a significant factor in risk assessment.
- **🎂 age:** Age at evaluation, as risk typically increases with age.
- **💔 cp (Chest Pain Type):** Types of chest pain (0-3).
- **💉 resting_BP:** Resting blood pressure (mm Hg).
- **🩸 chol:** Cholesterol level (mg/dL), where high levels increase risk.
- **🍬 fbs:** Fasting blood sugar level; values over 120 mg/dL indicate diabetes risk.
- **📈 restecg:** Resting ECG results; values range from 0-2.
- **🏃‍♂️ thalach:** Maximum heart rate achieved, a key cardiovascular metric.
- **❌ exang:** Exercise-induced angina (0: No, 1: Yes).
- **📉 oldpeak:** ST depression during exercise vs. rest, indicating potential ischemia.
- **📐 slope:** Slope of ST segment during peak exercise (0-2).
- **🩺 ca:** Number of major vessels blocked, ranging from 0 to 3.
- **🌡️ thal:** Thalassemia type (1: normal, 2: fixed defect, 3: reversible defect).
- **💖 Max Heart Rate Reserve:** Calculated max heart rate vs. recorded heart rate.
- **📊 Heart Disease Risk Score:** Quantified likelihood of developing heart disease.
- **🎯 target:** Presence of heart disease (0: No, 1: Yes).

---

### **🛠️ Data Preprocessing**

To prepare the dataset for modeling:

- **Categorical Encoding** 🧩: Converted 'sex' into numerical format (male = 1, female = 0).
- **Normalization** 🔄: Used MinMax scaling to keep values between 0 and 1 for balanced model training.
- **Feature Selection** ✅: Retained all features to maximize predictive power.
- **Train-Test Split** 📊: Used 80% of data for training and 20% for testing.

---

### **📈 Machine Learning Model Evaluation**

We trained four machine learning models on the dataset and evaluated each using accuracy, F1 score, precision, and recall:

| **Model**               | **Accuracy** | **F1 Score** | **Precision** | **Recall** |
|-------------------------|--------------|--------------|---------------|------------|
| 🌲 **Random Forest**     | 1.000        | 1.000        | 1.000         | 1.000      |
| ⚡ **Gradient Boosting** | 0.985        | 0.988        | 1.000         | 0.976      |
| ✳️ **Support Vector**    | 0.894        | 0.911        | 0.911         | 0.911      |
| 📉 **Logistic Regression** | 0.850      | 0.877        | 0.860         | 0.895      |

---

### **🧠 Deep Learning Model Evaluation**

A deep learning model was also implemented with a sequential neural network using:

- **Input Layer**: 64 nodes, ReLU activation
- **Hidden Layers**: Two layers (32 and 16 nodes), ReLU activation
- **Output Layer**: 1 node, sigmoid activation for binary classification

The model achieved:

- **Accuracy**: 0.947
- **F1 Score**: 0.954

---

### **🔑 Key Observations**

- **Random Forest**: Achieved perfect scores, but we should apply cross-validation to verify its generalizability.
- **Gradient Boosting**: Nearly matched Random Forest, balancing recall and precision effectively.
- **Support Vector and Logistic Regression**: Provided simpler baselines, offering interpretability with reasonable accuracy.
- **Deep Learning Model**: Performed well but didn't surpass classical models, likely due to dataset size limitations.

---

### **✅ Conclusion**

The analysis shows that **Random Forest** and **Gradient Boosting** are highly effective, with Random Forest achieving perfect metrics. The **Heart Disease Dataset** is rich with information, making it ideal for predictive analysis:

- **Random Forest** shows high reliability but should be validated further to prevent overfitting.
- **Explainability tools** like SHAP values can help interpret the Random Forest model, increasing trust in clinical applications.

### **🚀 Recommendations**

- **Further validation** of Random Forest to ensure robustness across new data, potentially through cross-validation.
- **Enhanced feature engineering** to boost simpler models like Logistic Regression.
- **Explainability** for healthcare adoption, using SHAP or feature importance plots.

This baseline analysis sets the stage for potential **real-world deployment** in healthcare, where the model can aid in **real-time decision support** for clinicians.

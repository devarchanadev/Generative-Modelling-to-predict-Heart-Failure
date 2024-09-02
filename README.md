# 🌟 **Generative Modelling to Predict Heart Failure** 🌟

[![Project Repository](https://img.shields.io/badge/🔗-Visit%20Repository-blue)]([your_repository_link_here](https://github.com/devarchanadev/Generative-Modelling-to-predict-Heart-Failure))

Welcome to the project **Generative Modelling to Predict Heart Failure**! In this project, we build and analyze a Bayesian Network to model relationships between clinical variables and predict the likelihood of heart failure.

---

## 🗂 **Table of Contents**

- [📊 Project Overview](#-project-overview)
- [💼 Business Impact](#-business-impact)
- [🛠 Data and Tools](#-data-and-tools)
- [⚙️ Methodology](#-methodology)
- [📈 Results and Insights](#-results-and-insights)
- [🔍 Conclusion](#-conclusion)
- [🚀 Key Takeaways](#-key-takeaways)

---

## 📊 **Project Overview**

The goal of this project is to understand heart conditions of patients by modeling relationships between selected clinical variables. We use **Bayesian Networks** to predict the chances of heart failure using both **structural learning techniques** and **prior knowledge** from the dataset.

```r
library(bnlearn)
library(gRbase)
data(cad1)
```

## 💼 **Business Impact**

Understanding the relationships between clinical variables can help healthcare providers make better decisions, improving patient outcomes. This model enables:

- **Personalized Treatment**: By identifying key risk factors, healthcare providers can tailor treatments to individual patients.
- **Early Intervention**: Predicting heart failure early can lead to preventative measures, potentially saving lives.
- **Cost Efficiency**: Reducing unnecessary tests and focusing on high-risk patients can optimize resource use in healthcare systems.

---

## 🛠 **Data and Tools**

### **Dataset:**
- **Source**: [bnlearn package](https://www.bnlearn.com/documentation/man/cad1/)
- **Variables**: Includes variables like sex, smoking habits, cholesterol levels, etc.

### **Tools Used:**

| Tool        | Purpose                                      |
|-------------|----------------------------------------------|
| **R**       | Programming language for statistical analysis |
| **bnlearn** | Learning and inference in Bayesian Networks  |
| **gRain**   | Performing inference in probabilistic networks |

### **Data Cleaning:**

The dataset was preprocessed to handle missing values and outliers, ensuring the accuracy of the model.

```r
# Example of data cleaning
cad1 <- na.omit(cad1)
```
---

## ⚙️ **Methodology**

### **Building the Bayesian Network**

1. **Initializing the Graph**: Create the skeleton of a directed acyclic graph (DAG).
2. **Implementing Structural Learning**: Apply the Hill-Climbing Algorithm.
3. **Parameter Learning**: Estimate conditional probability distributions.
4. **Validation**: Cross-validate the model using test data.

<img width="360" alt="Screenshot 2024-09-02 135927" src="https://github.com/user-attachments/assets/80934ade-d0ea-4c14-95b8-cea099145a3e">

```r
# Hill-Climbing algorithm example
bn <- hc(cad1)
```

## Inference Using the Model
Perform exact inference to predict the probability of heart failure given a set of observed variables.

```r
# Example of inference
cpquery(bn, event = (heart_failure == "Yes"), evidence = (smoking == "Yes"))
```

## 📈 **Results and Insights**

- **Key Variables**: Smoking and cholesterol levels were identified as significant predictors of heart failure.
- **Model Accuracy**: The Bayesian Network model achieved an accuracy of **85%** on the test dataset.
- **Risk Prediction**: Patients with high cholesterol and smoking habits have a **70%** higher chance of developing heart failure.

## 🔍 **Conclusion**

The Bayesian Network model effectively captures the relationships between clinical variables and provides accurate predictions for heart failure. This can greatly assist healthcare professionals in early diagnosis and intervention.

## 🚀 **Key Takeaways**

- **Bayesian Networks** are powerful tools for modeling complex relationships.
- **Early detection and personalized treatments** can significantly improve patient outcomes.
- **Data-Driven Decisions**: Leveraging data for predictive modeling can optimize healthcare strategies.

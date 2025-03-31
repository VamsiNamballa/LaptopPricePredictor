# 💻 Laptop Price Predictor (XLMiner-based ML Project)

A supervised machine learning project built using **XLMiner in Excel**, aimed at predicting the price of laptops based on hardware and software specifications.

> 🔍 **Tools Used**: Excel, XLMiner Add-in  
> 📊 **ML Algorithms**: Linear Regression, Regression Trees  
> 📁 **Dataset Source**: [Brand Laptops Dataset on Kaggle](https://www.kaggle.com/datasets/bhavikjikadara/brand-laptops-dataset)

---

## 📌 Project Overview

This project is part of the course **ISM6136 – Data Mining and Predictive Analytics**. We explore a dataset containing details of 992 laptops and build supervised ML models to predict the **price** of a laptop using various features such as processor, RAM, storage, GPU, display size, and OS.

---

## 📂 Dataset Details

- **Total Records (Original)**: 992  
- **Final Records (After Preprocessing)**: 705  
- **Target Variable**: `Price` (continuous numeric value)  
- **Key Features Used**:
  - Processor brand & tier
  - Number of cores & threads
  - RAM size
  - GPU brand & type
  - Display size, resolution
  - Operating system
  - Warranty duration

---

## 🧹 Data Preprocessing

- Removed irrelevant columns (`Index`, `Model`)
- Handled missing values using XLMiner’s `Missing Data Handling`
- Encoded categorical variables using `Create Dummies`
- Reduced feature cardinality for brand, RAM, OS, etc.
- Final dataset: 705 records × selected transformed features

---

## 📈 ML Models Built

### 1. **Linear Regression**
- Built 5 models using different feature combinations
- Used dummy variables and partitioned data (60:40)
- Evaluated using:
  - `Training R²`, `Validation R²`
  - `Training RMSE`, `Validation RMSE`
- **Best Model**: Model #4 (Highest R², lowest RMSE)
- Tried PCA on one model → Resulted in lower accuracy (<70%)

### 2. **Regression Trees**
- Built 5 models using XLMiner's Regression Tree
- Pruned using validation error and cost complexity
- Evaluated 3 tree types:
  - Fully Grown Tree
  - Minimum Error Tree
  - Best Pruned Tree
- **Best Model**: Model #1
- PCA again didn’t improve performance significantly

---

## 📊 Model Comparison

| Model Type         | Best Model | Validation R² | Validation RMSE | PCA Performance |
|--------------------|------------|----------------|------------------|------------------|
| Linear Regression  | Model #4   | ✅ > 70%        | ✅ Low            | ❌ Not Effective |
| Regression Tree    | Model #1   | ✅ > 70%        | ✅ Low            | ❌ Not Effective |

> **Conclusion**: Linear Regression was the best-performing algorithm for this dataset.

---

## 🚀 Deployment

- Final predictions made using the best models
- New test dataset (57 records) created and scored in XLMiner
- Output saved in `Scoring_LinearRegression` and `Scoring_DecisionTree`

---

## 📌 Learnings & Takeaways

- Hands-on experience with data preprocessing in Excel
- Applied and compared multiple ML models using XLMiner
- Understood limitations of PCA on certain datasets
- Learned the importance of validation metrics in model selection

---

## 🔮 Future Work

- Rebuild this project using **Python (pandas, scikit-learn, Streamlit)**  
- Explore **model interpretability tools** like SHAP or LIME  
- Deploy the final model as a **web app** or via a **REST API**

---

## 📧 Contact

**Pavan Vamsi Namballa**  
Student, M.S. in Data Science and Analytics  
✉️ [vamsman1234@gmail.com]  
🔗 [https://www.linkedin.com/in/pavan-vamsi-namballa/]

---

> ⭐ If you found this project helpful, please consider starring this repo!

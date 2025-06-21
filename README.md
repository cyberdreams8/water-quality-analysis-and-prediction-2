# 💧 Water Quality Classification using Machine Learning

This project aims to predict whether water is **potable (safe to drink)** based on various physicochemical properties. It enhances the baseline Kaggle dataset by incorporating **additional real-world data**, resulting in a more robust and practical classification model.

---

## 📌 Objective

To develop an accurate machine learning classifier that determines the potability of water samples, accounting for physicochemical attributes and real-world variances across **locations and time**. The goal is to support environmental agencies and public utilities in **automating water quality monitoring**.

---

## 📂 Project Files

- `modified_water_quality.ipynb` – Main Jupyter Notebook with:
  - Data cleaning & merging
  - Exploratory Data Analysis (EDA)
  - Feature scaling and handling of class imbalance
  - Supervised learning model development
  - Model evaluation and interpretation

---

## 🧾 Dataset Overview

### 🗂️ Source Datasets:
1. **Primary Dataset**:  
   [Kaggle – Water Potability Dataset](https://www.kaggle.com/datasets/adityakadiwal/water-potability)
   
2. **Additional Data**:  
   - Collected from publicly available sources and APIs  
   - Includes regional/location metadata, water body type (e.g., river, borewell), and time of collection  
   - Spans **5–6 years** across multiple regions

### 📌 Features:

| Feature Name         | Description                                 |
|----------------------|---------------------------------------------|
| `ph`                | Acidity/alkalinity level                    |
| `Hardness`          | Mineral content causing water hardness      |
| `Solids`            | Total dissolved solids (TDS)                |
| `Chloramines`       | Disinfectant compounds in water             |
| `Sulfate`           | Sulfate ion concentration                   |
| `Conductivity`      | Electrical conductivity of water            |
| `Organic_carbon`    | Level of organic matter                     |
| `Trihalomethanes`   | Harmful byproducts of chlorination          |
| `Turbidity`         | Clarity of water                            |
| `Region`            | New feature — geographic location           |
| `Water_Body`        | Type of source (e.g., lake, groundwater)    |
| `Collection_Year`   | Year of sampling                            |
| `Potability`        | Target variable (0 = Not potable, 1 = Potable) |

---

## 🔄 Data Preprocessing Steps

- Imputed missing values using feature-wise strategies
- Normalized features using **StandardScaler**
- Used **SMOTE** to balance the target classes
- Merged datasets and engineered temporal & categorical features

---

## 🧠 Models Used

- ✅ Logistic Regression  
- ✅ Random Forest Classifier  
- ✅ XGBoost Classifier  

Performance evaluated using:

- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix
- ROC-AUC Score
- Cross-validation

---

## 📈 Results

| Model              | Accuracy | F1 Score | ROC-AUC |
|--------------------|----------|----------|---------|
| Logistic Regression | ~74%     | ~0.73     | ~0.76   |
| Random Forest       | ~84%     | ~0.83     | ~0.89   |
| XGBoost             | ~86%     | ~0.85     | ~0.91   |

- XGBoost achieved the **highest performance** across all metrics.
- Feature importance revealed `ph`, `Trihalomethanes`, `Sulfate`, and `Organic_carbon` as most influential.

---

## 📊 Visualizations

- Distribution plots for each feature
- Correlation heatmap
- Confusion matrices
- ROC curves
- Feature importance bar charts

---

## 🧪 Use Cases

- Real-time water quality alerts using IoT sensors
- Planning water purification strategies
- Public health monitoring in low-resource settings
- Decision support for environmental agencies

---

## 🛠️ Installation

### Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn
```

# 💎 Diamond Price Prediction Model

## 🧑‍💻 Project by Team Penguins in [(SHAI For AI | شاي للذكاء الاصطناعي)](https://www.linkedin.com/company/shaiforai/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_recent_activity_content_view%3Byj4U18EwRQGZdBMsmHrBkA%3D%3D) training.

This project aims to predict diamond prices using a **Random Forest** model. Our focus was on building a robust model by performing detailed data preprocessing, feature engineering, and hyperparameter tuning. The model is capable of predicting diamond prices based on various features such as carat weight, cut, color, and clarity.

---

## 🔍 Project Overview
In this project, we used a dataset containing diamond features to predict their prices. The pipeline involves:
- Data cleaning and preprocessing (handling missing values, removing duplicates, and fixing outliers using IQR and clustering).
- Label Encoding **Ordinal Encoder**.
- Feature scaling with **StandardScaler**.
- **Feature engineering** for creating new features to improve model performance.
- **RandomizedSearchCV** for fine-tuning the **Random Forest** model.

## 🗂️ Dataset Overview
The dataset includes the following features:
1. **Carat**: Weight of the diamond.
2. **Cut**: Quality of the diamond's cut (e.g., Ideal, Premium).
3. **Color**: Diamond color grading.
4. **Clarity**: How clear the diamond is.
5. **Depth**: Total depth percentage.
6. **Table**: Width of the diamond's top as a percentage of its widest point.
7. **Price**: Price of the diamond in USD (target variable).
8. **Dimensions**: Measurements for length (x), width (y), and depth (z).

---

## 🛠️ Data Processing Steps

### 1️⃣ Exploratory Data Analysis (EDA)
- Identified and removed duplicates.
- Detected and handled missing or faulty data (e.g., rows with zeros in the `x`, `y`, `z` columns were removed).
- Outlier treatment using **log transformation** and the **Interquartile Range (IQR)** method to handle extreme values.
  
### 2️⃣ Data Preprocessing
- Encoded categorical variables (e.g., **Cut**, **Color**, and **Clarity**) using **Ordinal Encoder** to preserve the feature’s inherent order.
- Split the dataset into **80% training** and **20% testing** subsets.
- Applied **StandardScaler** for feature scaling to normalize data for better model performance.

---

## 🏗️ Feature Engineering
- Created two new features:
  1. **Table percentage**: Derived from the table and diamond dimensions (`x`, `y`, `z`).
  2. **Depth percentage**: Derived from the depth and diamond dimensions.
  
- Applied **Standard Scaling** to ensure uniformity across all numerical features.

---

## 🎯 Model Selection & Evaluation
We evaluated several models using **10-fold Cross-Validation** based on **Root Mean Squared Error (RMSE)**:
- **Linear Regression**
- **Lasso Regression**
- **Ridge Regression**
- **Decision Tree**
- **Random Forest** 🌟 (Best performer)
- **SVR**
- **Gradient Boosting**
- **XGBoost**

After cross-validation, the **Random Forest** and **XGBoost** models were selected due to their superior performance, with **Random Forest** yielding an RMSE of **553.66**.

---

## 🎛️ Model Fine-Tuning
Using **RandomizedSearchCV**, we fine-tuned the hyperparameters for **Random Forest**:
- **RMSE**: 545
- **Best Parameters**: `n_estimators=166`, `max_features=13`

---

## 🚀 How to Run the Project
1. Clone the repository.
2. Open the `diamond-price-model.ipynb` file in **VS Code** or **Jupyter Notebook**.
3. Run all the cells to preprocess the data, train the model, and generate predictions.

```bash
# Clone this repository
git clone https://github.com/AlharthAlhajHussein/Diamond-Price-Predictions-Model.git

# Open the Jupyter Notebook or VS Code to run
```

---

## 📊 Results

Final model performance after fine-tuning:

  **RMSE** (Root Mean Square Error): **531**

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps to contribute:
1. Fork the repository.
2. Create a new feature branch (`git checkout -b feature-branch`).
3. Make your changes and test them.
4. Submit a pull request.
   
---

## 👥 Team Penguins

 - الحارث بشار الحاج حسين
 - رغد عامر الحلبي
 - عمرو علي عبد الله
 - منار محمد سيد

---

## Copyrights

Made with 🤍 by **Penguins Team**

---

## 🌐 Follow Me

- [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alharth-alhaj-hussein-023417241)  
- [![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AlharthAlhajHussein)   
- [![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@Alharth.Alhaj.Hussein)
- [![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/alharthalhajhussein)



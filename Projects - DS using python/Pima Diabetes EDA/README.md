# 🏥 Diabetes Prediction System using Machine Learning

A robust machine learning pipeline designed to predict the diagnostic outcome of diabetes in patients based on the Pima Indians Diabetes Dataset. This project utilizes **K-Nearest Neighbors (KNN)** classification, extensive **Exploratory Data Analysis (EDA)**, and **Hyperparameter Tuning**.

## 📌 Project Overview

The goal of this project is to build a predictive model that can accurately classify whether a patient has diabetes based on diagnostic measures such as Glucose level, BMI, Insulin, and Age.

**Key Achievements:**

- Implemented a complete Data Science lifecycle (Data Cleaning → EDA → Scaling → Modeling → Evaluation).
- Optimized model performance using **GridSearchCV**.
- Visualized complex data relationships using **Seaborn** and **Matplotlib**.
- Solved version compatibility issues with modern visualization libraries.

## 🛠️ Tech Stack

- **Language:** Python 3.x
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Seaborn, Matplotlib (v3.x compatible)
- **Machine Learning:** Scikit-Learn (Sklearn)
- **Environment:** Google Colab / Jupyter Notebook

## 📂 Dataset

**Source:** Pima Indians Diabetes Database (National Institute of Diabetes and Digestive and Kidney Diseases).
**Rows:** 768
**Columns:** 9 (Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age, Outcome)

## ⚙️ Key Features & Workflow

### 1. Data Preprocessing

- Loaded dataset and checked for structural integrity (Shape, Null values, Duplicates).
- **Handling Missing Values:** Identified zero-values in columns like Glucose/Insulin (physiologically impossible) and treated them as missing data.

### 2. Exploratory Data Analysis (EDA)

- **Correlation Heatmap:** Analyzed relationships between features (e.g., Age vs. Pregnancies).
- **Box Plots:** Detected outliers in Insulin and BMI columns.
- **Pair Plots:** Visualized class separability between Diabetic vs. Non-Diabetic patients.
- **Histograms:** Checked the distribution of data (Normal vs. Skewed).

### 3. Feature Engineering

- **Standard Scaling:** Applied `StandardScaler` to normalize features. This is crucial for KNN, which relies on distance calculations (Euclidean distance).

### 4. Model Building (KNN)

- Split data into **Training (80%)** and **Testing (20%)** sets.
- Implemented the **K-Nearest Neighbors Classifier**.

### 5. Hyperparameter Tuning (Optimization)

- **Elbow Method:** Plotted Training vs. Testing accuracy for K values (1 to 25) to visually identify the best K.
- **GridSearchCV:** implemented automated tuning to find the mathematically optimal `n_neighbors`.
- *Constraint Fix:* Limited search range to `range(1, 50)` to strictly adhere to validation fold limits (avoiding `ValueError` on small datasets).

### 6. Evaluation

- **Accuracy Score:** Achieved optimal accuracy at **K=13**.
- **Confusion Matrix:** Analyzed True Positives and False Negatives to understand clinical risk.
- **Classification Report:** Generated Precision, Recall, and F1-Scores.

## 📊 Results

- **Optimal K Value:** 13
- **Max Testing Accuracy:** ~75-78% (varies based on random state split)

## 🐛 Technical Challenges & Fixes

During development, the following specific technical issues were resolved:

1. **Seaborn Syntax Update:** Fixed `TypeError` in `sns.lineplot` by strictly defining `x` and `y` arguments (required in Seaborn v0.12+).
2. **GridSearch Range:** Adjusted `n_neighbors` search space to ensure it did not exceed the sample size available in Cross-Validation folds.

## 📜

This project is open-source and available under the MIT License.

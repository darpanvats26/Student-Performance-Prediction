# Student-Performance-Prediction

## Project Overview

This project performs Exploratory Data Analysis (EDA) and Machine Learning on a **Student Habits and Performance** dataset. The goal is to understand which factors are associated with students' exam scores and build models to predict student performance.

The analysis includes both:

* **Regression:** Predicting the student's `exam_score`
* **Classification:** Predicting whether a student will **Pass or Fail**

## Dataset

The dataset contains **1,000 student records and 16 columns**.

Important variables include:

* Study hours per day
* Attendance percentage
* Sleep hours
* Social media hours
* Netflix hours
* Exercise frequency
* Mental health rating
* Diet quality
* Internet quality
* Parental education level
* Extracurricular participation
* Exam score

The dataset contains **91 missing values** in `parental_education_level`, which are handled during preprocessing.

## EDA

The exploratory analysis includes:

* Dataset structure and summary statistics
* Numerical and categorical variable identification
* Missing-value analysis
* Distribution analysis
* Boxplots for potential outliers
* Correlation matrix
* Feature relationships with `exam_score`
* Analysis of categorical variables against exam performance

The average exam score in the dataset is approximately **69.60**, with a median of **70.50**.

## Data Preprocessing

The following preprocessing steps are performed:

* `student_id` is excluded because it is an identifier.
* Missing numerical values are handled using median imputation.
* Missing categorical values are handled using most-frequent imputation.
* Categorical variables are converted using One-Hot Encoding.
* Numerical features are standardized using `StandardScaler`.

## Regression Model

A **Linear Regression** model is trained to predict `exam_score`.

Regression evaluation metrics include:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

Training and testing performance are compared to check the model's generalization and identify possible overfitting or underfitting.

## Classification Model

The regression target is converted into a binary classification target:

* **Pass:** Exam score ≥ 50
* **Fail:** Exam score < 50

A **Logistic Regression** model is then trained using the prepared features.

The classification model is evaluated using:

* Confusion Matrix
* Accuracy
* Precision
* Recall
* F1-Score

## Key Findings

The analysis indicates that **study hours are strongly associated with exam performance**. Other student lifestyle and behavioral factors, including mental health, social media usage, Netflix usage, sleep, and exercise, are also examined for their relationship with exam scores.

The regression and classification models are evaluated on both training and testing datasets to determine how well they generalize to unseen student data.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Files

* `Student_Performance_Prediction.ipynb` — Complete EDA, preprocessing, regression, classification, evaluation, and conclusions.
* `Day18_19_student_habits_performance.csv` — Student habits and performance dataset.

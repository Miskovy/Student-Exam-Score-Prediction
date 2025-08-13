# Student-Exam-Score-Prediction
This repository contains a Jupyter Notebook that explores various factors influencing student exam performance and builds a regression model to predict exam scores. The project demonstrates a full data science workflow, from initial data exploration and visualization to feature engineering and model evaluation.

## 📋 Table of Contents
- Project Overview

- Dataset

- Methodology

- Results and Performance

- Key Visualizations

- How to Run

- Requirements

## 🚀 Project Overview <a name="project-overview"></a>

The primary objective of this project is to understand the relationship between various student-related factors and their final exam scores. We build and evaluate several regression models to predict these scores, starting with a simple single-feature model and progressing to a more comprehensive multi-feature model.

The notebook covers:

1- Exploratory Data Analysis (EDA): Visualizing the data to uncover trends, distributions, and correlations between different factors and exam scores.

2- Data Cleaning: Identifying and handling missing values, duplicates, and incorrect data types.

3- Modeling:

 - Training a Simple Linear Regression model using only Hours_Studied.

 - Experimenting with Polynomial Regression to capture non-linear relationships.

 - Building a Multiple Linear Regression model using all relevant features for a more accurate prediction.

4- Evaluation: Comparing the performance of the different models using metrics like R-squared (R²) and Mean Squared Error (MSE).

## 💾 Dataset <a name="dataset"></a>

This project utilizes the Student Performance Factors dataset from Kaggle. You can access the dataset [here.](https://www.google.com/search?q=https://www.kaggle.com/datasets/subhamjain/loan-approval-prediction-dataset)

The dataset includes 20 different factors for 6,607 students, such as:

- Academic: Hours_Studied, Previous_Scores, Teacher_Quality

- Personal: Sleep_Hours, Physical_Activity, Motivation_Level

- Socio-Economic: Parental_Involvement, Family_Income, Access_to_Resources

- Target Variable: Exam_Score

## 🛠️ Methodology <a name="methodology"></a>

The project follows a structured approach to model building and evaluation.

1. Exploratory Data Analysis (EDA)
- Univariate Analysis: Histograms and count plots were used to examine the distribution of individual features like Exam_Score and Parental_Involvement.

- Bivariate Analysis: Scatter plots, box plots, and violin plots were created to explore the relationships between pairs of variables (e.g., Exam_Score vs. Hours_Studied).

- Multivariate Analysis: A correlation heatmap was generated for all numerical features to identify multicollinearity and strong predictors.

2. Data Cleaning

- Missing Values: Columns with missing data (Teacher_Quality, Parental_Education_Level, Distance_from_Home) were identified.

- Duplicates: The dataset was checked for and cleared of any duplicate entries.

- Data Types: Object columns were converted to the more efficient category data type.

3. Modeling and Feature Engineering

- Model 1 (Simple Linear Regression): A baseline model was created using only Hours_Studied to predict Exam_Score. This revealed a very weak correlation.

- Model 2 (Polynomial Regression): A second-degree polynomial model was tested on Hours_Studied but showed no significant improvement.

- Model 3 (Multiple Linear Regression): To build a more robust model, all categorical features were converted to a numerical format using one-hot encoding. This final model incorporates the combined predictive power of all factors.

## 📊 Results and Performance <a name="results-and-performance"></a>

The evaluation clearly showed that a multi-feature approach is far more effective for this dataset.

| Model                        | R-squared (R²) | Mean Squared Error (MSE) |
| ---------------------------- | -------------- | ------------------------ |
| Simple Linear Regression     | 0.23           | 10.86                    |
| Polynomial Regression        | 0.23           | 10.84                    |
| **Multiple Linear Regression** | **0.77** | **3.26** |

The final Multiple Linear Regression model explains 77% of the variance in exam scores, a significant improvement over the single-feature models. The lower MSE of 3.26 also indicates that its predictions are much closer to the actual scores.

## ✨ Key Visualizations <a name="key-visualizations"></a>

- Distribution of Exam Scores: Shows a normal distribution of final scores.

- Exam Score vs. Hours Studied: Illustrates the weak positive correlation between study time and exam results.

- Correlation Matrix: Highlights Previous_Scores as the strongest numerical predictor of Exam_Score.

## 💻 How to Run <a name="how-to-run"></a>

1- Clone the repository:

<div class="command-block">
<pre>git clone https://github.com/your-username/student-score-prediction.git</pre>
</div>
<div class="command-block">
<pre>cd student-score-prediction</pre>
</div>

2- Create and activate a virtual environment:

<div class="command-block">
<pre>python -m venv venv</pre>
</div>
<div class="command-block">
<pre>source venv/bin/activate  # On Windows, use venv\Scripts\activate</pre>
</div>

3- Install the necessary packages:

<div class="command-block">
<pre>pip install -r requirements.txt</pre>
</div>

4- Launch Jupyter Notebook:

<div class="command-block">
<pre>jupyter notebook</pre>
</div>

5- Open and run the student-score-prediction.ipynb notebook.

## 📦 Requirements <a name="requirements"></a>

This project requires the following Python libraries:
<div class="command-block">
<pre>pandas
numpy
matplotlib
seaborn
scikit-learn</pre>
</div>

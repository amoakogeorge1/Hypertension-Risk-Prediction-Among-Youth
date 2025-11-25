🩺 Hypertension Risk Prediction Using Machine Learning
🔍 1. What Problem Does This Solve?

This project predicts the likelihood of a person developing hypertension using lifestyle, behavioral, and clinical features.

💡 2. Business / Public Health Impact

Hypertension is one of the leading causes of stroke, heart disease, and kidney failure—yet many cases remain undiagnosed until complications occur.

Using this model:

Early prediction helps clinicians target individuals who need screening.

A community health program could identify up to 97% of high-risk individuals (based on model accuracy).

Targeted interventions can reduce long-term healthcare costs associated with untreated hypertension.

🛠 3. What I Did

Loaded and cleaned a dataset containing demographic, lifestyle, and clinical variables.

Performed exploratory data analysis (EDA) with summary statistics and visualizations.

Encoded categorical variables and prepared the dataset for modeling.

Trained multiple machine-learning models:

Logistic Regression

Random Forest Classifier

Evaluated models using accuracy, F1-score, recall, and confusion matrices.

Identified key risk-driving features using feature importance.

Selected the Random Forest model (97% accuracy) as the best performer.

📌 4. Key Findings

Blood Pressure History is the strongest predictor of hypertension.

Other important factors include:

Age

Salt intake

Stress scores

BMI

Sleep duration

The Random Forest model showed:

97% accuracy

High sensitivity for detecting hypertensive individuals

Lifestyle and behavioral variables contributed significantly to prediction.

🧭 5. Recommended Actions

Based on model insights:

For Public Health Practitioners

Prioritize screening individuals with past BP history, high BMI, and high salt intake.

Increase awareness about stress management and sleep hygiene.

For Clinicians

Use model outputs to flag high-risk individuals during routine checks.

Combine model predictions with clinical judgement for early intervention.

For Community Health Programs

Design youth-focused education on salt diet, exercise, and stress.

Target early detection initiatives around campuses or communities.

🧪 6. How to Run the Notebook
Requirements

Python 3.10+

Kaggle / Jupyter / Colab environment

Required libraries:

pandas
numpy
matplotlib
seaborn
scikit-learn

Steps

Clone the repository:

git clone https://github.com/your-username/your-repo.git


Open the notebook in Jupyter, Kaggle, or Google Colab.

Ensure the hypertension dataset is available at:

/kaggle/input/hypertension-dataset/hypertension_dataset.csv


Run cells sequentially.

🚀 7. Future Work

Build a Streamlit dashboard for real-time predictions.

Deploy the model as an API using FastAPI or Flask.

Collect youth-specific data to create a model tailored for ages 18–35.

Add SHAP analysis for deeper model explainability.

Expand dataset with:

Dietary patterns

Physical activity logs

Genetic/family risk factors.

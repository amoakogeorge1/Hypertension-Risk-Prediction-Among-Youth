Here is an updated single `README.md` incorporating the author (Arif Miah) and Apache 2.0 license details.[1]

```markdown
# Hypertension Risk Prediction in Young Adults

This repository contains a reproducible machine learning project that predicts **hypertension risk** using demographic, lifestyle, and clinical history features. The goal is to build an end‑to‑end, storytelling notebook that not only trains accurate models but also explains **why** they work and **how** the results can inform prevention and screening strategies. [file:1]

The project is implemented in Python using a Kaggle hypertension dataset created by **Arif Miah**, and compares a simple **Logistic Regression** baseline with a more flexible **Random Forest** model. It is aimed at data science learners, health data enthusiasts, and anyone interested in applying ML to public health problems. [file:1]

---

## Project structure

- `hypertension-risk-prediction.ipynb`  
  Main Jupyter notebook containing:
  - Problem framing and objectives  
  - Data overview and exploratory data analysis (EDA)  
  - Data preparation and feature engineering  
  - Model training and evaluation (Logistic Regression, Random Forest)  
  - Model interpretation via feature importance  
  - Limitations, future work, and replication notes [file:1]

---

## Dataset

This project uses the **Hypertension Dataset** by **Arif Miah**, hosted on **Kaggle**, licensed under the **Apache 2.0 License**. Please refer to the Kaggle dataset page for full license terms. [file:1]

The dataset includes:

- Demographic variables (e.g., age)  
- Lifestyle factors (e.g., BMI, stress score, sleep duration, salt intake, exercise level, smoking status)  
- Clinical history (e.g., blood pressure history, medication use)  
- Target label: `Has_Hypertension` (Yes/No)

To comply with licensing and Kaggle’s terms, the dataset itself is **not** stored in this repository. Instead:

1. Go to Kaggle and search for the **Hypertension Dataset** by **Arif Miah**.  
2. Download `hypertension_dataset.csv`, or add the dataset as an input to a Kaggle Notebook.  
3. If running locally, place the CSV in a `data/` directory and update the path in the notebook if needed, e.g.:

```
file_path = "data/hypertension_dataset.csv"
df = pd.read_csv(file_path)
```

---

## How to run the notebook

### 1. Clone the repository

```
git clone https://github.com/<your-username>/hypertension-risk-prediction.git
cd hypertension-risk-prediction
```

### 2. Set up a Python environment

Using `conda` (example):

```
conda create -n hypertenv python=3.11 -y
conda activate hypertenv
pip install -r requirements.txt  # or install the packages below
```

Required packages:

- `pandas`  
- `numpy`  
- `matplotlib`  
- `seaborn`  
- `scikit-learn`  
- `jupyter`  

### 3. Add the dataset

- Download the Kaggle hypertension dataset by Arif Miah and place it under `data/`:

```
mkdir -p data
# move hypertension_dataset.csv into data/
```

- Ensure the path in the notebook matches the file location.

### 4. Run the notebook

Start Jupyter:

```
jupyter notebook
```

Open `hypertension-risk-prediction.ipynb` and run all cells from top to bottom to:

1. Load and inspect the dataset.  
2. Perform EDA (class balance, feature distributions, correlations).  
3. Handle missing values and encode categorical variables.  
4. Split and scale the data.  
5. Train and evaluate Logistic Regression and Random Forest models.  
6. Analyze feature importance and draw domain insights.  
7. Summarize limitations and future work. [file:1]

---

## Key results

- **Class balance**: Hypertension is nearly balanced in this sample (≈52% Yes, 48% No).  
- **Logistic Regression**  
  - Accuracy: **0.819**  
  - Hypertension precision: **0.83**, recall: **0.81**, F1: **0.82**  
- **Random Forest**  
  - Accuracy: **0.960**  
  - Hypertension precision: **0.95**, recall: **0.98**, F1: **0.96**  

Random Forest significantly reduces false negatives compared to Logistic Regression, making it more suitable for screening scenarios where missing hypertensive individuals is costly. [file:1]

Feature importance highlights: [file:1]

- **BP_History** (~29.5%) – strongest predictor.  
- **Age**, **Stress_Score**, **BMI**, **Salt_Intake**, **Sleep_Duration** – important lifestyle/physiological factors.  
- **Family_History** and **Smoking_Status** – moderate contributors.  

---

## How to extend or replicate

You can extend this project in several directions: [file:1]

- Try additional models such as Gradient Boosting, XGBoost, or LightGBM.  
- Use k‑fold cross‑validation for more robust performance estimates.  
- Experiment with different encodings for categorical variables (one‑hot, target encoding).  
- Add SHAP or partial dependence plots for deeper interpretability.  
- Wrap the trained model into an API or dashboard (e.g., Streamlit) for interactive risk estimation.

If you replicate or modify this work, feel free to open an issue or pull request with your improvements.

---

## Acknowledgements

- **Dataset**:  
  Hypertension dataset created by **Arif Miah**, available on Kaggle under the **Apache 2.0 License**. Please cite and credit the original author when using the data. [file:1]

- **AI assistance**:  
  Narrative structure, section organization, and some refinements to the modelling and interpretation were supported by an AI assistant (Perplexity). [file:1]

---

## Repository license

The **code and notebook** in this repository are released under the **Apache 2.0 License**, consistent with the dataset’s license. See the `LICENSE` file for full terms.

When using this project, ensure that you comply with both the repository license and the original Kaggle dataset license.
```

